---
UID: NF:processthreadsapi.IsProcessorFeaturePresent
title: IsProcessorFeaturePresent function (processthreadsapi.h)
description: Determines whether the specified processor feature is supported by the current computer.
helpviewer_keywords: ["IsProcessorFeaturePresent","IsProcessorFeaturePresent function","PF_3DNOW_INSTRUCTIONS_AVAILABLE","PF_ARM_64BIT_LOADSTORE_ATOMIC","PF_ARM_DIVIDE_INSTRUCTION_AVAILABLE","PF_ARM_EXTERNAL_CACHE_AVAILABLE","PF_ARM_FMAC_INSTRUCTIONS_AVAILABLE","PF_ARM_VFP_32_REGISTERS_AVAILABLE","PF_CHANNELS_ENABLED","PF_COMPARE64_EXCHANGE128","PF_COMPARE_EXCHANGE128","PF_COMPARE_EXCHANGE_DOUBLE","PF_FASTFAIL_AVAILABLE","PF_FLOATING_POINT_EMULATED","PF_FLOATING_POINT_PRECISION_ERRATA","PF_MMX_INSTRUCTIONS_AVAILABLE","PF_NX_ENABLED","PF_PAE_ENABLED","PF_RDTSC_INSTRUCTION_AVAILABLE","PF_RDWRFSGSBASE_AVAILABLE","PF_SECOND_LEVEL_ADDRESS_TRANSLATION","PF_SSE3_INSTRUCTIONS_AVAILABLE","PF_SSSE3_INSTRUCTIONS_AVAILABLE","PF_SSE4_1_INSTRUCTIONS_AVAILABLE","PF_SSE4_2_INSTRUCTIONS_AVAILABLE","PF_AVX_INSTRUCTIONS_AVAILABLE","PF_AVX2_INSTRUCTIONS_AVAILABLE","PF_AVX512F_INSTRUCTIONS_AVAILABLE","PF_VIRT_FIRMWARE_ENABLED","PF_XMMI64_INSTRUCTIONS_AVAILABLE","PF_XMMI_INSTRUCTIONS_AVAILABLE","PF_XSAVE_ENABLED","_win32_isprocessorfeaturepresent","base.isprocessorfeaturepresent","processthreadsapi/IsProcessorFeaturePresent"]
old-location: base\isprocessorfeaturepresent.htm
tech.root: processthreadsapi
ms.assetid: c58cfb0a-f40f-429c-abe9-83b6f038f612
ms.date: 02/02/2024
ms.keywords: IsProcessorFeaturePresent, IsProcessorFeaturePresent function, PF_3DNOW_INSTRUCTIONS_AVAILABLE, PF_ARM_64BIT_LOADSTORE_ATOMIC, PF_ARM_DIVIDE_INSTRUCTION_AVAILABLE, PF_ARM_EXTERNAL_CACHE_AVAILABLE, PF_ARM_FMAC_INSTRUCTIONS_AVAILABLE, PF_ARM_VFP_32_REGISTERS_AVAILABLE, PF_CHANNELS_ENABLED, PF_COMPARE64_EXCHANGE128, PF_COMPARE_EXCHANGE128, PF_COMPARE_EXCHANGE_DOUBLE, PF_FASTFAIL_AVAILABLE, PF_FLOATING_POINT_EMULATED, PF_FLOATING_POINT_PRECISION_ERRATA, PF_MMX_INSTRUCTIONS_AVAILABLE, PF_NX_ENABLED, PF_PAE_ENABLED, PF_RDTSC_INSTRUCTION_AVAILABLE, PF_RDWRFSGSBASE_AVAILABLE, PF_SECOND_LEVEL_ADDRESS_TRANSLATION, PF_SSE3_INSTRUCTIONS_AVAILABLE, PF_SSSE3_INSTRUCTIONS_AVAILABLE, PF_SSE4_1_INSTRUCTIONS_AVAILABLE, PF_SSE4_2_INSTRUCTIONS_AVAILABLE, PF_AVX_INSTRUCTIONS_AVAILABLE, PF_AVX2_INSTRUCTIONS_AVAILABLE, PF_AVX512F_INSTRUCTIONS_AVAILABLE, PF_VIRT_FIRMWARE_ENABLED, PF_XMMI64_INSTRUCTIONS_AVAILABLE, PF_XMMI_INSTRUCTIONS_AVAILABLE, PF_XSAVE_ENABLED, _win32_isprocessorfeaturepresent, base.isprocessorfeaturepresent, processthreadsapi/IsProcessorFeaturePresent
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsProcessorFeaturePresent
 - processthreadsapi/IsProcessorFeaturePresent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - Vertdll.dll
api_name:
 - IsProcessorFeaturePresent
---

# IsProcessorFeaturePresent function


## -description

Determines whether the specified processor feature is supported by the current computer.

## -parameters

### -param ProcessorFeature [in]

The processor feature to be tested. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PF_ARM_64BIT_LOADSTORE_ATOMIC"></a><a id="pf_arm_64bit_loadstore_atomic"></a><dl>
<dt><b>PF_ARM_64BIT_LOADSTORE_ATOMIC</b></dt>
<dt>25</dt>
</dl>
</td>
<td width="60%">
The 64-bit load/store atomic instructions are available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_ARM_DIVIDE_INSTRUCTION_AVAILABLE"></a><a id="pf_arm_divide_instruction_available"></a><dl>
<dt><b>PF_ARM_DIVIDE_INSTRUCTION_AVAILABLE</b></dt>
<dt>24</dt>
</dl>
</td>
<td width="60%">
The divide instructions are available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_ARM_EXTERNAL_CACHE_AVAILABLE"></a><a id="pf_arm_external_cache_available"></a><dl>
<dt><b>PF_ARM_EXTERNAL_CACHE_AVAILABLE</b></dt>
<dt>26</dt>
</dl>
</td>
<td width="60%">
The external cache is available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_ARM_FMAC_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_fmac_instructions_available"></a><dl>
<dt><b>PF_ARM_FMAC_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>27</dt>
</dl>
</td>
<td width="60%">
The floating-point multiply-accumulate instruction is available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_ARM_VFP_32_REGISTERS_AVAILABLE"></a><a id="pf_arm_vfp_32_registers_available"></a><dl>
<dt><b>PF_ARM_VFP_32_REGISTERS_AVAILABLE</b></dt>
<dt>18</dt>
</dl>
</td>
<td width="60%">
The VFP/Neon: 32 x 64bit register bank is present. This flag has the same meaning as <b>PF_ARM_VFP_EXTENDED_REGISTERS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_3DNOW_INSTRUCTIONS_AVAILABLE"></a><a id="pf_3dnow_instructions_available"></a><dl>
<dt><b>PF_3DNOW_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The 3D-Now instruction set is available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_CHANNELS_ENABLED"></a><a id="pf_channels_enabled"></a><dl>
<dt><b>PF_CHANNELS_ENABLED</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
The processor channels are enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_COMPARE_EXCHANGE_DOUBLE"></a><a id="pf_compare_exchange_double"></a><dl>
<dt><b>PF_COMPARE_EXCHANGE_DOUBLE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The atomic compare and exchange operation (cmpxchg) is available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_COMPARE_EXCHANGE128"></a><a id="pf_compare_exchange128"></a><dl>
<dt><b>PF_COMPARE_EXCHANGE128</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
The  atomic compare and exchange 128-bit operation (cmpxchg16b) is available.

<b>Windows Server 2003 and Windows XP/2000:  </b>This feature is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_COMPARE64_EXCHANGE128"></a><a id="pf_compare64_exchange128"></a><dl>
<dt><b>PF_COMPARE64_EXCHANGE128</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
The atomic compare 64 and exchange 128-bit operation (cmp8xchg16) is available.

<b>Windows Server 2003 and Windows XP/2000:  </b>This feature is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_FASTFAIL_AVAILABLE"></a><a id="pf_fastfail_available"></a><dl>
<dt><b>PF_FASTFAIL_AVAILABLE</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
_fastfail() is available.
 

</td>
</tr>
<tr>
<td width="40%"><a id="PF_FLOATING_POINT_EMULATED"></a><a id="pf_floating_point_emulated"></a><dl>
<dt><b>PF_FLOATING_POINT_EMULATED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Floating-point operations are emulated using a software emulator.

This function returns a nonzero value if floating-point operations are emulated; otherwise, it returns zero.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_FLOATING_POINT_PRECISION_ERRATA"></a><a id="pf_floating_point_precision_errata"></a><dl>
<dt><b>PF_FLOATING_POINT_PRECISION_ERRATA</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
On a Pentium, a floating-point precision error can occur in rare circumstances.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_MMX_INSTRUCTIONS_AVAILABLE"></a><a id="pf_mmx_instructions_available"></a><dl>
<dt><b>PF_MMX_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The MMX instruction set is available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_NX_ENABLED"></a><a id="pf_nx_enabled"></a><dl>
<dt><b>PF_NX_ENABLED</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Memory/data-execution-prevention">Data execution prevention</a> is enabled.

<b>Windows XP/2000:  </b>This feature is not supported until Windows XP with SP2 and Windows Server 2003 with SP1.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_PAE_ENABLED"></a><a id="pf_pae_enabled"></a><dl>
<dt><b>PF_PAE_ENABLED</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The processor is PAE-enabled. For more information, see 
<a href="/windows/desktop/Memory/physical-address-extension">Physical Address Extension</a>.

All x64 processors always return a nonzero value for this feature.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_RDTSC_INSTRUCTION_AVAILABLE"></a><a id="pf_rdtsc_instruction_available"></a><dl>
<dt><b>PF_RDTSC_INSTRUCTION_AVAILABLE</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The RDTSC instruction is available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_RDWRFSGSBASE_AVAILABLE"></a><a id="pf_rdwrfsgsbase_available"></a><dl>
<dt><b>PF_RDWRFSGSBASE_AVAILABLE</b></dt>
<dt>22</dt>
</dl>
</td>
<td width="60%">
RDFSBASE, RDGSBASE, WRFSBASE, and WRGSBASE instructions are available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_SECOND_LEVEL_ADDRESS_TRANSLATION"></a><a id="pf_second_level_address_translation"></a><dl>
<dt><b>PF_SECOND_LEVEL_ADDRESS_TRANSLATION</b></dt>
<dt>20</dt>
</dl>
</td>
<td width="60%">
Second Level Address Translation is supported by the hardware.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_SSE3_INSTRUCTIONS_AVAILABLE"></a><a id="pf_sse3_instructions_available"></a><dl>
<dt><b>PF_SSE3_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
The SSE3 instruction set is available.

<b>Windows Server 2003 and Windows XP/2000:  </b>This feature is not supported.
 
</td>
</tr>
<tr>
<td width="40%"><a id="PF_SSSE3_INSTRUCTIONS_AVAILABLE"></a><a id="pf_ssse3_instructions_available"></a><dl>
<dt><b>PF_SSSE3_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>36</dt>
</dl>
</td>
<td width="60%">
The SSSE3 instruction set is available.
 
</td>
</tr>
<tr>
<td width="40%"><a id="PF_SSE4_1_INSTRUCTIONS_AVAILABLE"></a><a id="pf_sse4_1_instructions_available"></a><dl>
<dt><b>PF_SSE4_1_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>37</dt>
</dl>
</td>
<td width="60%">
The SSE4_1 instruction set is available.
 
</td>
</tr>
<tr>
<td width="40%"><a id="PF_SSE4_2_INSTRUCTIONS_AVAILABLE"></a><a id="pf_sse4_2_instructions_available"></a><dl>
<dt><b>PF_SSE4_2_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>38</dt>
</dl>
</td>
<td width="60%">
The SSE4_2 instruction set is available.
 
</td>
</tr>
<tr>
<td width="40%"><a id="PF_AVX_INSTRUCTIONS_AVAILABLE"></a><a id="pf_avx_instructions_available"></a><dl>
<dt><b>PF_AVX_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>39</dt>
</dl>
</td>
<td width="60%">
The AVX instruction set is available.
 
</td>
</tr>
<tr>
<td width="40%"><a id="PF_AVX2_INSTRUCTIONS_AVAILABLE"></a><a id="pf_avx2_instructions_available"></a><dl>
<dt><b>PF_AVX2_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>40</dt>
</dl>
</td>
<td width="60%">
The AVX2 instruction set is available.
 
</td>
</tr>
<tr>
<td width="40%"><a id="PF_AVX512F_INSTRUCTIONS_AVAILABLE"></a><a id="pf_avx512f_instructions_available"></a><dl>
<dt><b>PF_AVX512F_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>41</dt>
</dl>
</td>
<td width="60%">
The AVX512F instruction set is available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_VIRT_FIRMWARE_ENABLED"></a><a id="pf_virt_firmware_enabled"></a><dl>
<dt><b>PF_VIRT_FIRMWARE_ENABLED</b></dt>
<dt>21</dt>
</dl>
</td>
<td width="60%">
Virtualization is enabled in the firmware and made available by the operating system.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_XMMI_INSTRUCTIONS_AVAILABLE"></a><a id="pf_xmmi_instructions_available"></a><dl>
<dt><b>PF_XMMI_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The SSE instruction set is available.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_XMMI64_INSTRUCTIONS_AVAILABLE"></a><a id="pf_xmmi64_instructions_available"></a><dl>
<dt><b>PF_XMMI64_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The SSE2 instruction set is available.

<b>Windows 2000:  </b>This feature is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_XSAVE_ENABLED"></a><a id="pf_xsave_enabled"></a><dl>
<dt><b>PF_XSAVE_ENABLED</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
The processor implements the XSAVE and XRSTOR instructions.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:  </b>This feature is not supported until Windows 7 and Windows Server 2008 R2.

</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V8_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v8_instructions_available"></a><dl>
<dt><b>PF_ARM_V8_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>29</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the Arm v8 instructions set.
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V8_CRYPTO_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v8_crypto_instructions_available"></a><dl>
<dt><b>PF_ARM_V8_CRYPTO_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>30</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the Arm v8 extra cryptographic instructions (for example, AES, SHA1 and SHA2).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V8_CRC32_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v8_crc32_instructions_available"></a><dl>
<dt><b>PF_ARM_V8_CRC32_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>31</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the Arm v8 extra CRC32 instructions.
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V81_ATOMIC_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v81_atomic_instructions_available"></a><dl>
<dt><b>PF_ARM_V81_ATOMIC_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>34</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the Arm v8.1 atomic instructions (for example, CAS, SWP).
</td>
</tr>
 
<tr>
<td width="40%"><a id="PF_ARM_V82_DP_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v82_dp_instructions_available"></a><dl>
<dt><b>PF_ARM_V82_DP_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>43</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the Arm v8.2 DP instructions (for example, SDOT, UDOT). This feature is optional in Arm v8.2 implementations and mandatory in Arm v8.4 implementations.
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V83_JSCVT_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v83_jscvt_instructions_available"></a><dl>
<dt><b>PF_ARM_V83_JSCVT_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>44</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the Arm v8.3 JSCVT instructions (for example, FJCVTZS).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V83_LRCPC_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v83_lrcpc_instructions_available"></a><dl>
<dt><b>PF_ARM_V83_LRCPC_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>45</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the Arm v8.3 LRCPC instructions (for example, LDAPR). Note that certain Arm v8.2 CPUs may optionally support the LRCPC instructions.
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>46</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE (Scalable Vector Extension) instructions (<b>FEAT_SVE</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE2_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve2_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE2_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>47</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE2 instructions (<b>FEAT_SVE2</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE2_1_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve2_1_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE2_1_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>48</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE2.1 instructions (<b>FEAT_SVE2p1</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_AES_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_aes_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_AES_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>49</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE AES instructions (<b>FEAT_SVE_AES</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_PMULL128_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_pmull128_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_PMULL128_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>50</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE 128-bit polynomial multiply long instructions (<b>FEAT_SVE_PMULL128</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_BITPERM_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_bitperm_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_BITPERM_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>51</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE bit permute instructions (<b>FEAT_SVE_BitPerm</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_BF16_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_bf16_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_BF16_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>52</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE BF16 (BFloat16) instructions (<b>FEAT_BF16</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_EBF16_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_ebf16_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_EBF16_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>53</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE EBF16 (Extended BFloat16) instructions (<b>FEAT_EBF16</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_B16B16_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_b16b16_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_B16B16_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>54</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE B16B16 instructions (<b>FEAT_SVE_B16B16</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_SHA3_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_sha3_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_SHA3_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>55</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE SHA-3 cryptographic instructions (<b>FEAT_SVE_SHA3</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_SM4_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_sm4_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_SM4_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>56</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE SM4 cryptographic instructions (<b>FEAT_SVE_SM4</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_I8MM_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_i8mm_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_I8MM_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>57</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE I8MM (Int8 matrix multiply) instructions (<b>FEAT_I8MM</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_F32MM_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_f32mm_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_F32MM_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>58</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE F32MM (FP32 matrix multiply) instructions (<b>FEAT_F32MM</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SVE_F64MM_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sve_f64mm_instructions_available"></a><dl>
<dt><b>PF_ARM_SVE_F64MM_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>59</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE F64MM (FP64 matrix multiply) instructions (<b>FEAT_F64MM</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_BMI2_INSTRUCTIONS_AVAILABLE"></a><a id="pf_bmi2_instructions_available"></a><dl>
<dt><b>PF_BMI2_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>60</dt>
</dl>
</td>
<td width="60%">
This x64 processor implements the BMI2 instruction set.
</td>
</tr>

<tr>
<td width="40%"><a id="PF_MOVDIR64B_INSTRUCTION_AVAILABLE"></a><a id="pf_movdir64b_instruction_available"></a><dl>
<dt><b>PF_MOVDIR64B_INSTRUCTION_AVAILABLE</b></dt>
<dt>61</dt>
</dl>
</td>
<td width="60%">
This x64 processor implements the MOVDIR64B instruction.
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_LSE2_AVAILABLE"></a><a id="pf_arm_lse2_available"></a><dl>
<dt><b>PF_ARM_LSE2_AVAILABLE</b></dt>
<dt>62</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the LSE2 atomic instructions (<b>FEAT_LSE2</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SHA3_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sha3_instructions_available"></a><dl>
<dt><b>PF_ARM_SHA3_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>64</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SHA-3 cryptographic instructions (<b>FEAT_SHA3</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SHA512_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sha512_instructions_available"></a><dl>
<dt><b>PF_ARM_SHA512_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>65</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SHA-512 cryptographic instructions (<b>FEAT_SHA512</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V82_I8MM_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v82_i8mm_instructions_available"></a><dl>
<dt><b>PF_ARM_V82_I8MM_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>66</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the I8MM (Int8 matrix multiply) NEON instructions (<b>FEAT_I8MM</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V82_FP16_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v82_fp16_instructions_available"></a><dl>
<dt><b>PF_ARM_V82_FP16_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>67</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the FP16 (half-precision floating point) NEON instructions (<b>FEAT_FP16</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V86_BF16_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v86_bf16_instructions_available"></a><dl>
<dt><b>PF_ARM_V86_BF16_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>68</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the BF16 (BFloat16) NEON instructions (<b>FEAT_BF16</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V86_EBF16_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v86_ebf16_instructions_available"></a><dl>
<dt><b>PF_ARM_V86_EBF16_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>69</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the EBF16 (Extended BFloat16) NEON instructions (<b>FEAT_EBF16</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>70</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME (Scalable Matrix Extension) instructions (<b>FEAT_SME</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME2_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme2_instructions_available"></a><dl>
<dt><b>PF_ARM_SME2_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>71</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME2 instructions (<b>FEAT_SME2</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME2_1_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme2_1_instructions_available"></a><dl>
<dt><b>PF_ARM_SME2_1_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>72</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME2.1 instructions (<b>FEAT_SME2p1</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME2_2_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme2_2_instructions_available"></a><dl>
<dt><b>PF_ARM_SME2_2_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>73</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME2.2 instructions (<b>FEAT_SME2p2</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_AES_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_aes_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_AES_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>74</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE AES instructions when in Streaming SVE mode (<b>FEAT_SSVE_AES</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_SBITPERM_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_sbitperm_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_SBITPERM_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>75</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE bit permute instructions when in Streaming SVE mode (<b>FEAT_SSVE_BitPerm</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_SF8MM4_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_sf8mm4_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_SF8MM4_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>76</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE FMMLA (widening, 4-way, FP8 to FP16) instruction when in Streaming SVE mode (<b>FEAT_SSVE_F8F16MM</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_SF8MM8_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_sf8mm8_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_SF8MM8_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>77</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE FMMLA (widening, 8-way, FP8 to FP32) instruction when in Streaming SVE mode (<b>FEAT_SSVE_F8F32MM</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_SF8DP2_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_sf8dp2_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_SF8DP2_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>78</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE2 FP8DOT2 instructions when in Streaming SVE mode (<b>FEAT_SSVE_FP8DOT2</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_SF8DP4_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_sf8dp4_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_SF8DP4_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>79</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE2 FP8DOT4 instructions when in Streaming SVE mode (<b>FEAT_SSVE_FP8DOT4</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_SF8FMA_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_sf8fma_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_SF8FMA_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>80</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SVE2 FP8FMA instructions when in Streaming SVE mode (<b>FEAT_SSVE_FP8FMA</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_F8F32_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_f8f32_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_F8F32_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>81</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME F8F32 instructions (<b>FEAT_SME_F8F32</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_F8F16_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_f8f16_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_F8F16_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>82</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME F8F16 instructions (<b>FEAT_SME_F8F16</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_F16F16_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_f16f16_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_F16F16_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>83</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME F16F16 instructions (<b>FEAT_SME_F16F16</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_B16B16_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_b16b16_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_B16B16_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>84</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME B16B16 instructions (<b>FEAT_SME_B16B16</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_F64F64_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_f64f64_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_F64F64_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>85</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME F64F64 instructions (<b>FEAT_SME_F64F64</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_I16I64_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_i16i64_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_I16I64_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>86</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME I16I64 instructions (<b>FEAT_SME_I16I64</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_LUTv2_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_lutv2_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_LUTv2_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>87</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements the SME LUTv2 instructions (<b>FEAT_SME_LUTv2</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_SME_FA64_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_sme_fa64_instructions_available"></a><dl>
<dt><b>PF_ARM_SME_FA64_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>88</dt>
</dl>
</td>
<td width="60%">
This Arm processor implements SME FA64 (Full AArch64 instruction set when in Streaming SVE mode) (<b>FEAT_SME_FA64</b>).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_UMONITOR_INSTRUCTION_AVAILABLE"></a><a id="pf_umonitor_instruction_available"></a><dl>
<dt><b>PF_UMONITOR_INSTRUCTION_AVAILABLE</b></dt>
<dt>89</dt>
</dl>
</td>
<td width="60%">
This x64 processor implements the UMONITOR instruction.
</td>
</tr>

</table>

## -returns

If the feature is supported, the return value is a nonzero value.

If the feature is not supported, the return value is zero.

If the HAL does not support detection of the feature, whether or not the hardware supports the feature, the return value is also zero.

## -remarks

Support for ``PF_SSSE3_INSTRUCTIONS_AVAILABLE`` through ``PF_AVX512F_INSTRUCTIONS_AVAILABLE`` were added in the Windows SDK (19041) and are supported by Windows 10, Version 2004 (May 2020 Update) or later.

Support for ``PF_ERMS_AVAILABLE``, ``PF_ARM_V82_DP_INSTRUCTIONS_AVAILABLE``, and ``PF_ARM_V83_JSCVT_INSTRUCTIONS_AVAILABLE`` were added in the Windows SDK (20348) and are supported by Windows 11 and Windows Server 2022.

The define ``PF_ARM_V83_LRCPC_INSTRUCTIONS_AVAILABLE`` was added in the Windows SDK (22621) and is supported by Windows 11, Version 22H2.

Support for ``PF_ARM_SVE_INSTRUCTIONS_AVAILABLE`` through ``PF_MOVDIR64B_INSTRUCTION_AVAILABLE`` and ``PF_ARM_SHA3_INSTRUCTIONS_AVAILABLE`` through ``PF_ARM_V86_EBF16_INSTRUCTIONS_AVAILABLE`` were added in the Windows SDK (26100) and are supported by Windows 11, version 24H2 and Windows Server 2025 or later.

## -see-also

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)

[System Information Functions](/windows/win32/SysInfo/system-information-functions)


