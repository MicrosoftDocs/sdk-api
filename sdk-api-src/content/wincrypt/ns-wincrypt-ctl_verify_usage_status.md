---
UID: NS:wincrypt._CTL_VERIFY_USAGE_STATUS
title: CTL_VERIFY_USAGE_STATUS
author: windows-sdk-content
description: Contains information about a Certificate Trust List (CTL) returned by CertVerifyCTLUsage.
old-location: security\ctl_verify_usage_status.htm
tech.root: seccrypto
ms.assetid: 2b7ef953-9422-4dcf-b293-a78a06bb080e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCTL_VERIFY_USAGE_STATUS, CTL_VERIFY_USAGE_STATUS, CTL_VERIFY_USAGE_STATUS structure [Security], PCTL_VERIFY_USAGE_STATUS, PCTL_VERIFY_USAGE_STATUS structure pointer [Security], _crypto2_ctl_verify_usage_status, security.ctl_verify_usage_status, wincrypt/CTL_VERIFY_USAGE_STATUS, wincrypt/PCTL_VERIFY_USAGE_STATUS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Wincrypt.h
api_name:
 - CTL_VERIFY_USAGE_STATUS
product: Windows
targetos: Windows
req.typenames: CTL_VERIFY_USAGE_STATUS, *PCTL_VERIFY_USAGE_STATUS
req.redist: 
---

# CTL_VERIFY_USAGE_STATUS structure


## -description


The <b>CTL_VERIFY_USAGE_STATUS</b> structure contains information about a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Trust List</a> (CTL) returned by 
<a href="https://msdn.microsoft.com/d87d8157-8e52-4198-bfd4-46d83d72eb13">CertVerifyCTLUsage</a>.


## -struct-fields




### -field cbSize

The size, in bytes, of the structure. The application calling 
<a href="https://msdn.microsoft.com/d87d8157-8e52-4198-bfd4-46d83d72eb13">CertVerifyCTLUsage</a> sets this parameter. If <b>cbSize</b> is not greater than or equal to the required size of the structure, <b>CertVerifyCTLUsage</b> returns <b>FALSE</b> and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>E_INVALIDARG</b>.


### -field dwError

The error status, if any, returned by the call to <a href="https://msdn.microsoft.com/d87d8157-8e52-4198-bfd4-46d83d72eb13">CertVerifyCTLUsage</a>. For the list of possible error values, see the Return Values section in <b>CertVerifyCTLUsage</b>.


### -field dwFlags

If <b>CERT_VERIFY_UPDATED_CTL_FLAG</b> is returned, <a href="https://msdn.microsoft.com/d87d8157-8e52-4198-bfd4-46d83d72eb13">CertVerifyCTLUsage</a> updated a CTL whose time was no longer valid with a new, time-valid CTL.


### -field ppCtl

Pointer to a pointer to a CTL <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> containing the matched subject. The calling application can set this pointer to <b>NULL</b> to indicate that a CTL containing the subject is not to be returned. 




If <b>ppCtl</b> is not <b>NULL</b>, the calling application must free the returned context using <a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>.


### -field dwCtlEntryIndex

Returns the array location of the matching subject's entry in the CTL's array.


### -field ppSigner

A pointer to a pointer to the certificate context of the signer of the CTL. This pointer can be set to <b>NULL</b> by the calling application indicating that the certificate of the signer of the CTL is not to be returned. 




If <b>ppSigner</b> is not <b>NULL</b>, the calling application must free the returned context using <a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>.


### -field dwSignerIndex

Index of the signer actually used. Needed if a message has more than one signer.


## -remarks



The members <b>dwError</b>, <b>dwFlags</b>, <b>dwCtlEntryIndex</b>, and <b>dwSignerIndex</b> should be initialized to zero by the calling application.




## -see-also




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/d87d8157-8e52-4198-bfd4-46d83d72eb13">CertVerifyCTLUsage</a>
 

 

