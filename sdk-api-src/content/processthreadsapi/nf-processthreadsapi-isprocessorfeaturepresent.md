---
UID: NF:processthreadsapi.IsProcessorFeaturePresent
title: IsProcessorFeaturePresent function (processthreadsapi.h)
description: Determines whether the specified processor feature is supported by the current computer.
helpviewer_keywords: ["IsProcessorFeaturePresent","IsProcessorFeaturePresent function","PF_3DNOW_INSTRUCTIONS_AVAILABLE","PF_ARM_64BIT_LOADSTORE_ATOMIC","PF_ARM_DIVIDE_INSTRUCTION_AVAILABLE","PF_ARM_EXTERNAL_CACHE_AVAILABLE","PF_ARM_FMAC_INSTRUCTIONS_AVAILABLE","PF_ARM_VFP_32_REGISTERS_AVAILABLE","PF_CHANNELS_ENABLED","PF_COMPARE64_EXCHANGE128","PF_COMPARE_EXCHANGE128","PF_COMPARE_EXCHANGE_DOUBLE","PF_FASTFAIL_AVAILABLE","PF_FLOATING_POINT_EMULATED","PF_FLOATING_POINT_PRECISION_ERRATA","PF_MMX_INSTRUCTIONS_AVAILABLE","PF_NX_ENABLED","PF_PAE_ENABLED","PF_RDTSC_INSTRUCTION_AVAILABLE","PF_RDWRFSGSBASE_AVAILABLE","PF_SECOND_LEVEL_ADDRESS_TRANSLATION","PF_SSE3_INSTRUCTIONS_AVAILABLE","PF_VIRT_FIRMWARE_ENABLED","PF_XMMI64_INSTRUCTIONS_AVAILABLE","PF_XMMI_INSTRUCTIONS_AVAILABLE","PF_XSAVE_ENABLED","_win32_isprocessorfeaturepresent","base.isprocessorfeaturepresent","processthreadsapi/IsProcessorFeaturePresent"]
old-location: base\isprocessorfeaturepresent.htm
tech.root: winprog
ms.assetid: c58cfb0a-f40f-429c-abe9-83b6f038f612
ms.date: 12/05/2018
ms.keywords: IsProcessorFeaturePresent, IsProcessorFeaturePresent function, PF_3DNOW_INSTRUCTIONS_AVAILABLE, PF_ARM_64BIT_LOADSTORE_ATOMIC, PF_ARM_DIVIDE_INSTRUCTION_AVAILABLE, PF_ARM_EXTERNAL_CACHE_AVAILABLE, PF_ARM_FMAC_INSTRUCTIONS_AVAILABLE, PF_ARM_VFP_32_REGISTERS_AVAILABLE, PF_CHANNELS_ENABLED, PF_COMPARE64_EXCHANGE128, PF_COMPARE_EXCHANGE128, PF_COMPARE_EXCHANGE_DOUBLE, PF_FASTFAIL_AVAILABLE, PF_FLOATING_POINT_EMULATED, PF_FLOATING_POINT_PRECISION_ERRATA, PF_MMX_INSTRUCTIONS_AVAILABLE, PF_NX_ENABLED, PF_PAE_ENABLED, PF_RDTSC_INSTRUCTION_AVAILABLE, PF_RDWRFSGSBASE_AVAILABLE, PF_SECOND_LEVEL_ADDRESS_TRANSLATION, PF_SSE3_INSTRUCTIONS_AVAILABLE, PF_VIRT_FIRMWARE_ENABLED, PF_XMMI64_INSTRUCTIONS_AVAILABLE, PF_XMMI_INSTRUCTIONS_AVAILABLE, PF_XSAVE_ENABLED, _win32_isprocessorfeaturepresent, base.isprocessorfeaturepresent, processthreadsapi/IsProcessorFeaturePresent
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
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
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
This ARM processor implements the ARM v8 instructions set.
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V8_CRYPTO_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v8_crypto_instructions_available"></a><dl>
<dt><b>PF_ARM_V8_CRYPTO_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>30</dt>
</dl>
</td>
<td width="60%">
This ARM processor implements the ARM v8 extra cryptographic instructions (i.e. AES, SHA1 and SHA2).
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V8_CRC32_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v8_crc32_instructions_available"></a><dl>
<dt><b>PF_ARM_V8_CRC32_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>31</dt>
</dl>
</td>
<td width="60%">
This ARM processor implements the ARM v8 extra CRC32 instructions.
</td>
</tr>

<tr>
<td width="40%"><a id="PF_ARM_V81_ATOMIC_INSTRUCTIONS_AVAILABLE"></a><a id="pf_arm_v81_atomic_instructions_available"></a><dl>
<dt><b>PF_ARM_V81_ATOMIC_INSTRUCTIONS_AVAILABLE</b></dt>
<dt>34</dt>
</dl>
</td>
<td width="60%">
This ARM processor implements the ARM v8.1 atomic instructions (e.g. CAS, SWP).
</td>
</tr>

</table>

## -returns

If the feature is supported, the return value is a nonzero value.

If the feature is not supported, the return value is zero.

If the HAL does not support detection of the feature, whether or not the hardware supports the feature, the return value is also zero.

## -see-also

<a href="/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
