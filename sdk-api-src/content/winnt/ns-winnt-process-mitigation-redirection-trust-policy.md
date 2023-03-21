---
UID: NS:winnt._PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY
title: PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY (winnt.h)
description: Contains process mitigation policy settings for the ???.
tech.root: backup
ms.assetid: 71345263-a825-40b3-90f7-3f62b0aa7f58
ms.date: 05/25/2022
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
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
req.typenames: PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY, *PPROCESS_MITIGATION_REDIRECTION_TRUST_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY
 - winnt/_PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY
 - PPROCESS_MITIGATION_REDIRECTION_TRUST_POLICY
 - winnt/PPROCESS_MITIGATION_REDIRECTION_TRUST_POLICY
 - PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY
 - winnt/PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY
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
 - PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY
---

# PROCESS_MITIGATION_REDIRECTION_TRUST_POLICY structure

## -description

Contains process mitigation policy settings for RedirectionGuard.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Flags

Reserved for system use.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.EnforceRedirectionTrust

Set (0x1) to prevent the process from following filesystem junctions created by non-admin users and log the attempt; otherwise leave unset (0x0).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditRedirectionTrust

Set (0x1) to log when the process follows filesystem junctions created by non-admin users, but still allow the operation; otherwise leave unset (0x0).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

Reserved for system use.

## -remarks

The [GetProcessMitigationPolicy](../processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy.md)  and [SetProcessMitigationPolicy](../processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy.md)  functions use this structure.

## -see-also
