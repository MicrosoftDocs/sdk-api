---
UID: NF:processthreadsapi.SetProcessMitigationPolicy
title: SetProcessMitigationPolicy function (processthreadsapi.h)
description: Sets a mitigation policy for the calling process. Mitigation policies enable a process to harden itself against various types of attacks.
helpviewer_keywords: ["ProcessASLRPolicy","ProcessControlFlowGuardPolicy","ProcessDEPPolicy","ProcessDynamicCodePolicy","ProcessExtensionPointDisablePolicy","ProcessFontDisablePolicy","ProcessImageLoadPolicy","ProcessMitigationOptionsMask","ProcessSignaturePolicy","ProcessStrictHandleCheckPolicy","ProcessSystemCallDisablePolicy","SetProcessMitigationPolicy","SetProcessMitigationPolicy function","base.setprocessmitigationpolicy","processthreadsapi/SetProcessMitigationPolicy"]
old-location: base\setprocessmitigationpolicy.htm
tech.root: ProcThread
ms.assetid: 57f364f8-58d7-447a-91c3-51fc1fe1a481
ms.date: 12/05/2018
ms.keywords: ProcessASLRPolicy, ProcessControlFlowGuardPolicy, ProcessDEPPolicy, ProcessDynamicCodePolicy, ProcessExtensionPointDisablePolicy, ProcessFontDisablePolicy, ProcessImageLoadPolicy, ProcessMitigationOptionsMask, ProcessSignaturePolicy, ProcessStrictHandleCheckPolicy, ProcessSystemCallDisablePolicy, SetProcessMitigationPolicy, SetProcessMitigationPolicy function, base.setprocessmitigationpolicy, processthreadsapi/SetProcessMitigationPolicy
f1_keywords:
- processthreadsapi/SetProcessMitigationPolicy
dev_langs:
- c++
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
- SetProcessMitigationPolicy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetProcessMitigationPolicy function


## -description


Sets a mitigation policy for the calling process. Mitigation policies enable a process to harden itself against various types of attacks.


## -parameters




### -param MitigationPolicy [in]

The mitigation policy to apply. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ProcessDEPPolicy"></a><a id="processdeppolicy"></a><a id="PROCESSDEPPOLICY"></a><dl>
<dt><b>ProcessDEPPolicy</b></dt>
</dl>
</td>
<td width="60%">
The data execution prevention (DEP) policy of the process.

The <i>lpBuffer</i> parameter points to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-process_mitigation_dep_policy">PROCESS_MITIGATION_DEP_POLICY</a> structure that specifies the DEP policy flags.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessASLRPolicy"></a><a id="processaslrpolicy"></a><a id="PROCESSASLRPOLICY"></a><dl>
<dt><b>ProcessASLRPolicy</b></dt>
</dl>
</td>
<td width="60%">
The Address Space Layout Randomization (ASLR) policy of the process.

The <i>lpBuffer</i> parameter points to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-process_mitigation_aslr_policy">PROCESS_MITIGATION_ASLR_POLICY</a> structure that specifies the ASLR policy flags.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessDynamicCodePolicy"></a><a id="processdynamiccodepolicy"></a><a id="PROCESSDYNAMICCODEPOLICY"></a><dl>
<dt><b>ProcessDynamicCodePolicy</b></dt>
</dl>
</td>
<td width="60%">
The dynamic code policy of the process. When turned on, the process cannot generate dynamic code or modify existing executable code.

The <i>lpBuffer</i> parameter points to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-process_mitigation_dynamic_code_policy">PROCESS_MITIGATION_DYNAMIC_CODE_POLICY</a> structure that specifies the dynamic code policy flags.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessStrictHandleCheckPolicy"></a><a id="processstricthandlecheckpolicy"></a><a id="PROCESSSTRICTHANDLECHECKPOLICY"></a><dl>
<dt><b>ProcessStrictHandleCheckPolicy</b></dt>
</dl>
</td>
<td width="60%">
The process will receive a fatal error if it manipulates a handle that is not valid.

The <i>lpBuffer</i> parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_strict_handle_check_policy">PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY</a> structure that specifies the handle check policy flags.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessSystemCallDisablePolicy"></a><a id="processsystemcalldisablepolicy"></a><a id="PROCESSSYSTEMCALLDISABLEPOLICY"></a><dl>
<dt><b>ProcessSystemCallDisablePolicy</b></dt>
</dl>
</td>
<td width="60%">
Disables the ability to use NTUser/GDI functions at the lowest layer.

The <i>lpBuffer</i> parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_system_call_disable_policy">PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY</a> structure that specifies the system call disable policy flags.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessMitigationOptionsMask"></a><a id="processmitigationoptionsmask"></a><a id="PROCESSMITIGATIONOPTIONSMASK"></a><dl>
<dt><b>ProcessMitigationOptionsMask</b></dt>
</dl>
</td>
<td width="60%">
Returns the mask of valid bits for all the mitigation options on the system.  An application can set many mitigation options without querying the operating system for mitigation options by combining bitwise with the mask to exclude all non-supported bits at once.

The <i>lpBuffer</i> parameter points to a <b>ULONG64</b> bit vector for the mask, or to accommodate more than 64 bits, a two-element array of <b>ULONG64</b> bit vectors.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessExtensionPointDisablePolicy"></a><a id="processextensionpointdisablepolicy"></a><a id="PROCESSEXTENSIONPOINTDISABLEPOLICY"></a><dl>
<dt><b>ProcessExtensionPointDisablePolicy</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpBuffer</i> parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy">PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY</a> structure that specifies the extension point disable policy flags.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessControlFlowGuardPolicy"></a><a id="processcontrolflowguardpolicy"></a><a id="PROCESSCONTROLFLOWGUARDPOLICY"></a><dl>
<dt><b>ProcessControlFlowGuardPolicy</b></dt>
</dl>
</td>
<td width="60%">
The Control Flow Guard (CFG) policy of the process.

The <i>lpBuffer</i> parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_control_flow_guard_policy">PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY</a> structure that specifies the CFG policy flags.

<div class="alert"><b>Note</b>  This value is not currently supported.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="ProcessSignaturePolicy"></a><a id="processsignaturepolicy"></a><a id="PROCESSSIGNATUREPOLICY"></a><dl>
<dt><b>ProcessSignaturePolicy</b></dt>
</dl>
</td>
<td width="60%">
The policy of a process that can restrict image loading to those images that are either signed by Microsoft, by the Windows Store, or by Microsoft, the Windows Store and the Windows Hardware Quality Labs (WHQL).

he <i>lpBuffer</i> parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_binary_signature_policy">PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY</a> structure that specifies the signature policy flags.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessFontDisablePolicy"></a><a id="processfontdisablepolicy"></a><a id="PROCESSFONTDISABLEPOLICY"></a><dl>
<dt><b>ProcessFontDisablePolicy</b></dt>
</dl>
</td>
<td width="60%">
The policy regarding font loading for the process. When turned on, the process cannot load non-system fonts.

The <i>lpBuffer</i> parameter points to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-process_mitigation_font_disable_policy">PROCESS_MITIGATION_FONT_DISABLE_POLICY</a> structure that specifies the policy flags for font loading.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessImageLoadPolicy"></a><a id="processimageloadpolicy"></a><a id="PROCESSIMAGELOADPOLICY"></a><dl>
<dt><b>ProcessImageLoadPolicy</b></dt>
</dl>
</td>
<td width="60%">
The policy regarding image loading for the process, which determines the types of executable images that are allowed to be mapped into the process. When turned on, images cannot be loaded from some locations, such a remote devices or files that have the low mandatory label.

The <i>lpBuffer</i> parameter points to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-process_mitigation_image_load_policy">PROCESS_MITIGATION_IMAGE_LOAD_POLICY</a> structure that specifies the policy flags for image loading.

</td>
</tr>
</table>
 


### -param lpBuffer [in]

If the <i>MitigationPolicy</i> parameter is <b>ProcessDEPPolicy</b>, this parameter points to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-process_mitigation_dep_policy">PROCESS_MITIGATION_DEP_POLICY</a> structure that specifies the DEP policy flags.

If the <i>MitigationPolicy</i> parameter is <b>ProcessASLRPolicy</b>, this parameter points to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-process_mitigation_aslr_policy">PROCESS_MITIGATION_ASLR_POLICY</a> structure that specifies the ASLR policy flags.

If the <i>MitigationPolicy</i> parameter is <b>ProcessImageLoadPolicy</b>, this parameter points to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-process_mitigation_image_load_policy">PROCESS_MITIGATION_IMAGE_LOAD_POLICY</a> structure that receives the policy flags for image loading.

If the <i>MitigationPolicy</i> parameter is <b>ProcessStrictHandleCheckPolicy</b>, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_strict_handle_check_policy">PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY</a> structure that specifies the handle check policy flags.

If the <i>MitigationPolicy</i> parameter is <b>ProcessSystemCallDisablePolicy</b>, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_system_call_disable_policy">PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY</a> structure that specifies the system call disable policy flags.

If the <i>MitigationPolicy</i> parameter is <b>ProcessMitigationOptionsMask</b>, this parameter points to a <b>ULONG64</b> bit vector for the mask, or to accommodate more than 64 bits, a two-element array of <b>ULONG64</b> bit vectors.

If the <i>MitigationPolicy</i> parameter is <b>ProcessExtensionPointDisablePolicy</b>, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy">PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY</a> structure that specifies the extension point disable policy flags.

If the <i>MitigationPolicy</i> parameter is <b>ProcessControlFlowGuardPolicy</b>, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_control_flow_guard_policy">PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY</a> structure that specifies the CFG policy flags.

If the <i>MitigationPolicy</i> parameter is <b>ProcessSignaturePolicy</b>, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_binary_signature_policy">PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY</a> structure that specifies the signature policy flags.

If the <i>MitigationPolicy</i> parameter is <b>ProcessFontDisablePolicy</b>, this parameter points to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-process_mitigation_font_disable_policy">PROCESS_MITIGATION_FONT_DISABLE_POLICY</a> structure that specifies the policy flags for font loading.

If the <i>MitigationPolicy</i> parameter is <b>ProcessImageLoadPolicy</b>, this parameter points to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-process_mitigation_image_load_policy">PROCESS_MITIGATION_IMAGE_LOAD_POLICY</a> structure that specifies the policy flags for image loading.


### -param dwLength [in]

The size of <i>lpBuffer</i>, in bytes.


## -returns



If the function succeeds, it returns <b>TRUE</b>. If the function fails, it returns <b>FALSE</b>. To retrieve error values defined for this function, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Setting mitigation policy for a process helps prevent an attacker from exploiting security vulnerabilities. Use the <b>SetProcessMitigationPolicy</b> function to enable or disable security mitigation programmatically.

For maximum effectiveness, mitigation policies should be applied before or during process initialization. For example, setting the ASLR policy that enables forced relocation of images is effective only if it is applied before all of the images in a process have been loaded.

ASLR mitigation policies cannot be made less restrictive after they have been applied. 

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0602. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.



