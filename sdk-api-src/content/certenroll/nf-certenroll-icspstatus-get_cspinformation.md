---
UID: NF:certenroll.ICspStatus.get_CspInformation
title: ICspStatus::get_CspInformation
author: windows-sdk-content
description: Retrieves an ICspInformation object that contains general information about the provider.
old-location: security\icspstatus_cspinformation.htm
old-project: SecCertEnroll
ms.assetid: 9e9202ad-086e-493b-8830-0a0f8980cec5
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CspInformation property [Security], CspInformation property [Security],ICspStatus interface, ICspStatus interface [Security],CspInformation property, ICspStatus.CspInformation, ICspStatus.get_CspInformation, ICspStatus::CspInformation, ICspStatus::get_CspInformation, certenroll/ICspStatus::CspInformation, certenroll/ICspStatus::get_CspInformation, get_CspInformation, security.icspstatus_cspinformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ICspStatus.CspInformation
-	ICspStatus.get_CspInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspStatus::get_CspInformation


## -description


The <b>CspInformation</b> property retrieves an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object that contains general information about the provider. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object includes the following information about a CSP:

<ul>
<li>A collection of supported algorithms and their intended uses.</li>
<li>Whether the CSP is implemented in hardware or software.</li>
<li>Whether the CSP is a smart card provider or a legacy provider.</li>
<li>The version number and name.</li>
<li>Whether the CSP is installed on the client computer.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a>



<a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a>
 

 

