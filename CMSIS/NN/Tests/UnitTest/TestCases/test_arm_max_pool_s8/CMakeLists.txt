#
# Copyright (C) 2010-2020 Arm Limited or its affiliates. All rights reserved.
#
# SPDX-License-Identifier: Apache-2.0
#
# Licensed under the Apache License, Version 2.0 (the License); you may
# not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an AS IS BASIS, WITHOUT
# WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

add_cmsis_nn_unit_test_executable(test_arm_max_pool_s8)

target_sources(test_arm_max_pool_s8 PRIVATE
    Unity/unity_test_arm_max_pool_s8.c
    Unity/TestRunner/unity_test_arm_max_pool_s8_runner.c
    ${CMSIS_PATH}/CMSIS/NN/Source/PoolingFunctions/arm_max_pool_s8.c)

target_include_directories(test_arm_max_pool_s8 PRIVATE ${CMSIS_PATH}/CMSIS/NN/Include)
target_include_directories(test_arm_max_pool_s8 PRIVATE ${CMSIS_PATH}/CMSIS/DSP/Include)
target_include_directories(test_arm_max_pool_s8 PRIVATE ${CMSIS_PATH}/CMSIS/Core/Include)

target_link_libraries(test_arm_max_pool_s8 LINK_PUBLIC unity)
