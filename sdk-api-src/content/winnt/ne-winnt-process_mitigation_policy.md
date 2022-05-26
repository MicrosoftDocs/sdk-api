---
UID: NE:winnt._PROCESS_MITIGATION_POLICY
title: PROCESS_MITIGATION_POLICY (winnt.h)
description: Represents the different process mitigation policies.
helpviewer_keywords: ["*PPROCESS_MITIGATION_POLICY","MaxProcessMitigationPolicy","PPROCESS_MITIGATION_POLICY","PPROCESS_MITIGATION_POLICY enumeration pointer","PROCESS_MITIGATION_POLICY","PROCESS_MITIGATION_POLICY enumeration","ProcessASLRPolicy","ProcessControlFlowGuardPolicy","ProcessDEPPolicy","ProcessDynamicCodePolicy","ProcessExtensionPointDisablePolicy","ProcessFontDisablePolicy","ProcessImageLoadPolicy","ProcessMitigationOptionsMask","ProcessSignaturePolicy","ProcessStrictHandleCheckPolicy","ProcessSystemCallDisablePolicy","base.process_mitigation_policy","winnt/MaxProcessMitigationPolicy","winnt/PPROCESS_MITIGATION_POLICY","winnt/PROCESS_MITIGATION_POLICY","winnt/ProcessASLRPolicy","winnt/ProcessControlFlowGuardPolicy","winnt/ProcessDEPPolicy","winnt/ProcessDynamicCodePolicy","winnt/ProcessExtensionPointDisablePolicy","winnt/ProcessFontDisablePolicy","winnt/ProcessImageLoadPolicy","winnt/ProcessMitigationOptionsMask","winnt/ProcessSignaturePolicy","winnt/ProcessStrictHandleCheckPolicy","winnt/ProcessSystemCallDisablePolicy"]
old-location: base\process_mitigation_policy.htm
tech.root: backup
ms.assetid: b9636a0f-3123-499d-8663-72ed4d4993f0
ms.date: 05/24/2022
ms.keywords: '*PPROCESS_MITIGATION_POLICY, MaxProcessMitigationPolicy, PPROCESS_MITIGATION_POLICY, PPROCESS_MITIGATION_POLICY enumeration pointer, PROCESS_MITIGATION_POLICY, PROCESS_MITIGATION_POLICY enumeration, ProcessASLRPolicy, ProcessControlFlowGuardPolicy, ProcessDEPPolicy, ProcessDynamicCodePolicy, ProcessExtensionPointDisablePolicy, ProcessFontDisablePolicy, ProcessImageLoadPolicy, ProcessMitigationOptionsMask, ProcessSignaturePolicy, ProcessStrictHandleCheckPolicy, ProcessSystemCallDisablePolicy, base.process_mitigation_policy, winnt/MaxProcessMitigationPolicy, winnt/PPROCESS_MITIGATION_POLICY, winnt/PROCESS_MITIGATION_POLICY, winnt/ProcessASLRPolicy, winnt/ProcessControlFlowGuardPolicy, winnt/ProcessDEPPolicy, winnt/ProcessDynamicCodePolicy, winnt/ProcessExtensionPointDisablePolicy, winnt/ProcessFontDisablePolicy, winnt/ProcessImageLoadPolicy, winnt/ProcessMitigationOptionsMask, winnt/ProcessSignaturePolicy, winnt/ProcessStrictHandleCheckPolicy, winnt/ProcessSystemCallDisablePolicy'
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROCESS_MITIGATION_POLICY, *PPROCESS_MITIGATION_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MITIGATION_POLICY
 - winnt/_PROCESS_MITIGATION_POLICY
 - PPROCESS_MITIGATION_POLICY
 - winnt/PPROCESS_MITIGATION_POLICY
 - PROCESS_MITIGATION_POLICY
 - winnt/PROCESS_MITIGATION_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - PROCESS_MITIGATION_POLICY
---

# PROCESS_MITIGATION_POLICY enumeration

## -description

Represents the different process mitigation policies.

## -enum-fields

### -field ProcessDEPPolicy

The data execution prevention (DEP) policy of the process.

### -field ProcessASLRPolicy

The Address Space Layout Randomization (ASLR) policy of the process.

### -field ProcessDynamicCodePolicy

The policy that turns off the ability of the process to generate dynamic code or modify existing executable code.

### -field ProcessStrictHandleCheckPolicy

The process will receive a fatal error if it manipulates an invalid handle. Useful for preventing downstream problems in a process due to handle misuse.

### -field ProcessSystemCallDisablePolicy

Disables the ability to use NTUser/GDI functions at the lowest layer.

### -field ProcessMitigationOptionsMask

Returns the mask of valid bits for all the mitigation options on the system.  An application can set many mitigation options without querying the operating system for mitigation options by combining bitwise with the mask to exclude all non-supported bits at once.

### -field ProcessExtensionPointDisablePolicy

The policy that prevents some built-in third party extension points from being turned on, which prevents legacy extension point DLLs from being loaded into the process.

### -field ProcessControlFlowGuardPolicy

The Control Flow Guard (CFG) policy of the process.

### -field ProcessSignaturePolicy

The policy of a process that can restrict image loading to those images that are either signed by Microsoft, by the Windows Store, or by Microsoft, the Windows Store and the Windows Hardware Quality Labs (WHQL).

### -field ProcessFontDisablePolicy

The policy that turns off the ability of the process to load non-system fonts.

### -field ProcessImageLoadPolicy

The policy that turns off the ability of the process to load images from some locations, such a remote devices or files that have the low mandatory label.

### -field ProcessSystemCallFilterPolicy

The system call filter policy of the process.

### -field ProcessPayloadRestrictionPolicy

The payload restriction policy of the process.

### -field ProcessChildProcessPolicy

The child process policy of the process.

### -field ProcessSideChannelIsolationPolicy

The side channel isolation policy of the process.

### -field ProcessUserShadowStackPolicy

Windows 10, version 2004 and above: The policy regarding user-mode Hardware-enforced Stack Protection for the process.

### -field ProcessRedirectionTrustPolicy

The RedirectionGuard policy of the process.

### -field ProcessUserPointerAuthPolicy

The user pointer authentication policy of the process.

### -field ProcessSEHOPPolicy

The Structured Exception Handling Overwrite Protection (SEHOP) policy of the process.

### -field MaxProcessMitigationPolicy

Ends the enumeration.

## -remarks

## -see-also

[GetProcessMitigationPolicy function](../processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy.md), [SetProcessMitigationPolicy function](../processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy.md)