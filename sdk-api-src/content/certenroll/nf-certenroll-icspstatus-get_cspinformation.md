---
UID: NF:certenroll.ICspStatus.get_CspInformation
title: ICspStatus::get_CspInformation (certenroll.h)
description: Retrieves an ICspInformation object that contains general information about the provider.
helpviewer_keywords: ["CspInformation property [Security]","CspInformation property [Security]","ICspStatus interface","ICspStatus interface [Security]","CspInformation property","ICspStatus.CspInformation","ICspStatus.get_CspInformation","ICspStatus::CspInformation","ICspStatus::get_CspInformation","certenroll/ICspStatus::CspInformation","certenroll/ICspStatus::get_CspInformation","get_CspInformation","security.icspstatus_cspinformation"]
old-location: security\icspstatus_cspinformation.htm
tech.root: security
ms.assetid: 9e9202ad-086e-493b-8830-0a0f8980cec5
ms.date: 12/05/2018
ms.keywords: CspInformation property [Security], CspInformation property [Security],ICspStatus interface, ICspStatus interface [Security],CspInformation property, ICspStatus.CspInformation, ICspStatus.get_CspInformation, ICspStatus::CspInformation, ICspStatus::get_CspInformation, certenroll/ICspStatus::CspInformation, certenroll/ICspStatus::get_CspInformation, get_CspInformation, security.icspstatus_cspinformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspStatus::get_CspInformation
 - certenroll/ICspStatus::get_CspInformation
dev_langs:
 - c++
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
---

# ICspStatus::get_CspInformation


## -description

The <b>CspInformation</b> property retrieves an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object that contains general information about the provider. This property is web enabled.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object includes the following information about a CSP:

<ul>
<li>A collection of supported algorithms and their intended uses.</li>
<li>Whether the CSP is implemented in hardware or software.</li>
<li>Whether the CSP is a smart card provider or a legacy provider.</li>
<li>The version number and name.</li>
<li>Whether the CSP is installed on the client computer.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a>