---
UID: NF:processthreadsapi.GetProcessMitigationPolicy
title: GetProcessMitigationPolicy function (processthreadsapi.h)
description: Retrieves mitigation policy settings for the calling process.
helpviewer_keywords: ["GetProcessMitigationPolicy","GetProcessMitigationPolicy function","ProcessASLRPolicy","ProcessControlFlowGuardPolicy","ProcessDEPPolicy","ProcessDynamicCodePolicy","ProcessExtensionPointDisablePolicy","ProcessFontDisablePolicy","ProcessImageLoadPolicy","ProcessMitigationOptionsMask","ProcessSideChannelIsolationPolicy","ProcessSignaturePolicy","ProcessStrictHandleCheckPolicy","ProcessSystemCallDisablePolicy","base.getprocessmitigationpolicy","processthreadsapi/GetProcessMitigationPolicy"]
old-location: base\getprocessmitigationpolicy.htm
tech.root: processthreadsapi
ms.assetid: 89f9c883-6976-4af2-9a8b-c76101d8ed02
ms.date: 12/05/2018
ms.keywords: GetProcessMitigationPolicy, GetProcessMitigationPolicy function, ProcessASLRPolicy, ProcessControlFlowGuardPolicy, ProcessDEPPolicy, ProcessDynamicCodePolicy, ProcessExtensionPointDisablePolicy, ProcessFontDisablePolicy, ProcessImageLoadPolicy, ProcessMitigationOptionsMask, ProcessSideChannelIsolationPolicy, ProcessSignaturePolicy, ProcessStrictHandleCheckPolicy, ProcessSystemCallDisablePolicy, ProcessUserShadowStackPolicy, base.getprocessmitigationpolicy, processthreadsapi/GetProcessMitigationPolicy
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
ms.custom: RS5, 19H1
f1_keywords:
 - GetProcessMitigationPolicy
 - processthreadsapi/GetProcessMitigationPolicy
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
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetProcessMitigationPolicy
---

# GetProcessMitigationPolicy function


## -description

Retrieves mitigation policy settings for the calling process.

## -parameters

### -param hProcess [in]

A handle to the process. This handle must have the PROCESS_QUERY_INFORMATION access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param MitigationPolicy [in]

The mitigation policy to retrieve. This parameter can be one of the following values.

|Value  |Meaning  |
|---------|---------|
|**ProcessDEPPolicy**     | The data execution prevention (DEP) policy of the process.<br/>The *lpBuffer* parameter points to a <a href="/windows/desktop/api/winnt/ns-winnt-process_mitigation_dep_policy">PROCESS_MITIGATION_DEP_POLICY</a> structure that specifies the DEP policy flags.        |
| **ProcessASLRPolicy** | The Address Space Layout Randomization (ASLR) policy of the process.<br/>The *lpBuffer* parameter points to a <a href="/windows/desktop/api/winnt/ns-winnt-process_mitigation_aslr_policy">PROCESS_MITIGATION_ASLR_POLICY</a> structure that specifies the ASLR policy flags. |
| **ProcessDynamicCodePolicy** | The dynamic code policy of the process. When turned on, the process cannot generate dynamic code or modify existing executable code.<br/>The *lpBuffer* parameter points to a <a href="/windows/desktop/api/winnt/ns-winnt-process_mitigation_dynamic_code_policy">PROCESS_MITIGATION_DYNAMIC_CODE_POLICY</a> structure that specifies the dynamic code policy flags. |
| **ProcessStrictHandleCheckPolicy** | The process will receive a fatal error if it manipulates a handle that is not valid.<br/>The *lpBuffer* parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_strict_handle_check_policy">PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY</a> structure that specifies the handle check policy flags. |
| **ProcessSystemCallDisablePolicy** | Disables the ability to use NTUser/GDI functions at the lowest layer.<br/>The *lpBuffer* parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_system_call_disable_policy">PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY</a> structure that specifies the system call disable policy flags. |
| **ProcessMitigationOptionsMask** | Returns the mask of valid bits for all the mitigation options on the system.  An application can set many mitigation options without querying the operating system for mitigation options by combining bitwise with the mask to exclude all non-supported bits at once.<br/>The *lpBuffer* parameter points to a **ULONG64** bit vector for the mask, or a two-element array of **ULONG64** bit vectors. |
| **ProcessExtensionPointDisablePolicy** | Prevents certain built-in third party extension points from being enabled, preventing legacy extension point DLLs from being loaded into the process.<br/>The *lpBuffer* parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy">PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY</a> structure that specifies the extension point disable policy flags. |
| **ProcessControlFlowGuardPolicy** | The Control Flow Guard (CFG) policy of the process.<br/>The *lpBuffer* parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_control_flow_guard_policy">PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY</a> structure that specifies the CFG policy flags. |
| **ProcessSignaturePolicy** | The policy of a process that can restrict image loading to those images that are either signed by Microsoft, by the Windows Store, or by Microsoft, the Windows Store and the Windows Hardware Quality Labs (WHQL).<br/>he *lpBuffer* parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_binary_signature_policy">PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY</a> structure that specifies the signature policy flags. |
| **ProcessFontDisablePolicy** | The policy regarding font loading for the process. When turned on, the process cannot load non-system fonts.<br/>The *lpBuffer* parameter points to a <a href="/windows/desktop/api/winnt/ns-winnt-process_mitigation_font_disable_policy">PROCESS_MITIGATION_FONT_DISABLE_POLICY</a> structure that specifies the policy flags for font loading. |
| **ProcessImageLoadPolicy** | The policy regarding image loading for the process, which determines the types of executable images that are allowed to be mapped into the process. When turned on, images cannot be loaded from some locations, such a remote devices or files that have the low mandatory label.<br/>The *lpBuffer* parameter points to a <a href="/windows/desktop/api/winnt/ns-winnt-process_mitigation_image_load_policy">PROCESS_MITIGATION_IMAGE_LOAD_POLICY</a> structure that specifies the policy flags for image loading. |
| **ProcessRedirectionTrustPolicy** | The RedirectionGuard policy of a process. The *lpBuffer* parameter points to a [PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY](../winnt/ns-winnt-process-mitigation-redirection-trust-policy.md) structure that specifies the mitigation mode. |
| **ProcessSideChannelIsolationPolicy** | Windows 10, version 1809 and above: The policy regarding isolation of side channels for the specified process.<br/>The *lpBuffer* parameter points to a <a href="../winnt/ns-winnt-process_mitigation_side_channel_isolation_policy.md">PROCESS_MITIGATION_SIDE_CHANNEL_ISOLATION_POLICY</a> structure that specifies the policy flags for side channel isolation. |
| **ProcessUserShadowStackPolicy** | Windows 10, version 2004 and above: The policy regarding user-mode Hardware-enforced Stack Protection for the specified process.<br/>The *lpBuffer* parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_user_shadow_stack_policy">PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY</a> structure that specifies the policy flags for user-mode Hardware-enforced Stack Protection.
 |
### -param lpBuffer [out]

If the *MitigationPolicy* parameter is **ProcessDEPPolicy**, this parameter points to a <a href="/windows/desktop/api/winnt/ns-winnt-process_mitigation_dep_policy">PROCESS_MITIGATION_DEP_POLICY</a> structure that receives the DEP policy flags.

If the *MitigationPolicy* parameter is **ProcessASLRPolicy**, this parameter points to a <a href="/windows/desktop/api/winnt/ns-winnt-process_mitigation_aslr_policy">PROCESS_MITIGATION_ASLR_POLICY</a> structure that receives the ASLR policy flags.

If the *MitigationPolicy* parameter is **ProcessDynamicCodePolicy**, this parameter points to a <a href="/windows/desktop/api/winnt/ns-winnt-process_mitigation_dynamic_code_policy">PROCESS_MITIGATION_DYNAMIC_CODE_POLICY</a> structure that receives the dynamic code policy flags.

If the *MitigationPolicy* parameter is **ProcessStrictHandleCheckPolicy**, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_strict_handle_check_policy">PROCESS_MITIGATION_STRICT_HANDLE_CHECK_POLICY</a> structure that specifies the handle check policy flags.

If the *MitigationPolicy* parameter is **ProcessSystemCallDisablePolicy**, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_system_call_disable_policy">PROCESS_MITIGATION_SYSTEM_CALL_DISABLE_POLICY</a> structure that specifies the system call disable policy flags.

If the *MitigationPolicy* parameter is **ProcessMitigationOptionsMask**, this parameter points to a **ULONG64** bit vector for the mask or a two-element array of **ULONG64** bit vectors.

If the *MitigationPolicy* parameter is **ProcessExtensionPointDisablePolicy**, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy">PROCESS_MITIGATION_EXTENSION_POINT_DISABLE_POLICY</a> structure that specifies the extension point disable policy flags.

If the *MitigationPolicy* parameter is **ProcessControlFlowGuardPolicy**, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_control_flow_guard_policy">PROCESS_MITIGATION_CONTROL_FLOW_GUARD_POLICY</a> structure that specifies the CFG policy flags.

If the *MitigationPolicy* parameter is **ProcessSignaturePolicy**, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_binary_signature_policy">PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY</a> structure that receives the signature policy flags.

If the *MitigationPolicy* parameter is **ProcessFontDisablePolicy**, this parameter points to a <a href="/windows/desktop/api/winnt/ns-winnt-process_mitigation_font_disable_policy">PROCESS_MITIGATION_FONT_DISABLE_POLICY</a> structure that receives the policy flags for font loading.

If the *MitigationPolicy* parameter is **ProcessImageLoadPolicy**, this parameter points to a <a href="/windows/desktop/api/winnt/ns-winnt-process_mitigation_image_load_policy">PROCESS_MITIGATION_IMAGE_LOAD_POLICY</a> structure that receives the policy flags for image loading.

If the *MitigationPolicy* parameter is **ProcessRedirectionTrustPolicy**, this parameter points to a [PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY structure](../winnt/ns-winnt-process-mitigation-redirection-trust-policy.md) that specifies the mitigation mode.

If the *MitigationPolicy* parameter is **ProcessUserShadowStackPolicy**, this parameter points to a <a href="/windows/win32/api/winnt/ns-winnt-process_mitigation_user_shadow_stack_policy">PROCESS_MITIGATION_USER_SHADOW_STACK_POLICY</a> structure that receives the policy flags for user-mode Hardware-enforced Stack Protection.

### -param dwLength [in]

The size of *lpBuffer*, in bytes.

## -returns

If the function succeeds, it returns **TRUE**. If the function fails, it returns **FALSE**. To retrieve error values defined for this function, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0602. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.
