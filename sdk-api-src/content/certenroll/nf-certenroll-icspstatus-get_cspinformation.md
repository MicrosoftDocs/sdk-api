---
UID: NF:certenroll.ICspStatus.get_CspInformation
title: ICspStatus::get_CspInformation
author: windows-sdk-content
description: Retrieves an ICspInformation object that contains general information about the provider.
old-location: security\icspstatus_cspinformation.htm
tech.root: SecCertEnroll
ms.assetid: 9e9202ad-086e-493b-8830-0a0f8980cec5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CspInformation property [Security], CspInformation property [Security],ICspStatus interface, ICspStatus interface [Security],CspInformation property, ICspStatus.CspInformation, ICspStatus.get_CspInformation, ICspStatus::CspInformation, ICspStatus::get_CspInformation, certenroll/ICspStatus::CspInformation, certenroll/ICspStatus::get_CspInformation, get_CspInformation, security.icspstatus_cspinformation
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspStatus.CspInformation
 - ICspStatus.get_CspInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- ICspStatus.get_CspInformation
: 
---

# ICspStatus::get_CspInformation


## -description


The <b>CspInformation</b> property retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> object that contains general information about the provider. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> object includes the following information about a CSP:

<ul>
<li>A collection of supported algorithms and their intended uses.</li>
<li>Whether the CSP is implemented in hardware or software.</li>
<li>Whether the CSP is a smart card provider or a legacy provider.</li>
<li>The version number and name.</li>
<li>Whether the CSP is installed on the client computer.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a>
 

 

