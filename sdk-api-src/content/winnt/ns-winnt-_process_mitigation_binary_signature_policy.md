---
UID: NS:winnt._PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
title: "_PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY"
author: windows-sdk-content
description: Contains process mitigation policy settings for the loading of images depending on the signatures for the image.
old-location: base\process_mitigation_binary_signature_policy.htm
tech.root: procthread
ms.assetid: 581D6D0C-0480-45A1-9C76-2A269C46D27B
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY structure pointer, PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY structure, _PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, base.process_mitigation_binary_signature_policy, winnt/PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, winnt/PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
product: Windows
targetos: Windows
req.typenames: PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY, *PPROCESS_MITIGATION_BINARY_SIGNATURE_POLICY
req.redist: 
---

# _PROCESS_MITIGATION_BINARY_SIGNATURE_POLICY structure


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




<a href="https://msdn.microsoft.com/89f9c883-6976-4af2-9a8b-c76101d8ed02">GetProcessMitigationPolicy</a>



<a href="https://msdn.microsoft.com/57f364f8-58d7-447a-91c3-51fc1fe1a481">SetProcessMitigationPolicy</a>
 

 

