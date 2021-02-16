---
UID: NS:winnt._PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
title: PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY (winnt.h)
description: Contains process mitigation policy settings for the loading of images depending on the signatures for the image.
helpviewer_keywords: ["*PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY","PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY","PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY structure pointer","PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY","PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY structure","base.process_mitigation_binary_signature_policy","winnt/PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY","winnt/PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY"]
old-location: base\process_mitigation_binary_signature_policy.htm
tech.root: backup
ms.assetid: 581D6D0C-0480-45A1-9C76-2A269C46D27B
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY structure pointer, PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY structure, base.process_mitigation_binary_signature_policy, winnt/PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, winnt/PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, *PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
 - winnt/_PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
 - PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
 - winnt/PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
 - PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
 - winnt/PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
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
 - PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
---

# PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY structure


## -description

Contains process mitigation policy settings for the loading of images depending on the signatures for the image.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Flags

Reserved for system use.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.MicrosoftSignedOnly

Set (0x1) to prevent the process from loading images that are not signed by Microsoft; otherwise leave unset (0x0).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.StoreSignedOnly

Set (0x1) to prevent the process from loading images that are not signed by the Windows Store; otherwise leave unset (0x0).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.MitigationOptIn

Set (0x1) to prevent the process from loading images that are not signed by Microsoft, the Windows Store and the Windows Hardware Quality Labs (WHQL); otherwise leave unset (0x0).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditMicrosoftSignedOnly

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.AuditStoreSignedOnly

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ReservedFlags

Reserved for system use.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy">GetProcessMitigationPolicy</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy">SetProcessMitigationPolicy</a>