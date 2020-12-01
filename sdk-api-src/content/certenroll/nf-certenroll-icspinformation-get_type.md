---
UID: NF:certenroll.ICspInformation.get_Type
title: ICspInformation::get_Type (certenroll.h)
description: Retrieves the type of the provider.
helpviewer_keywords: ["ICspInformation interface [Security]","Type property","ICspInformation.Type","ICspInformation.get_Type","ICspInformation::Type","ICspInformation::get_Type","Type property [Security]","Type property [Security]","ICspInformation interface","certenroll/ICspInformation::Type","certenroll/ICspInformation::get_Type","get_Type","security.icspinformation_type_property"]
old-location: security\icspinformation_type_property.htm
tech.root: security
ms.assetid: a52caea6-fbd5-4c06-8a25-e65f7b4a72f7
ms.date: 12/05/2018
ms.keywords: ICspInformation interface [Security],Type property, ICspInformation.Type, ICspInformation.get_Type, ICspInformation::Type, ICspInformation::get_Type, Type property [Security], Type property [Security],ICspInformation interface, certenroll/ICspInformation::Type, certenroll/ICspInformation::get_Type, get_Type, security.icspinformation_type_property
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
 - ICspInformation::get_Type
 - certenroll/ICspInformation::get_Type
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
 - ICspInformation.Type
 - ICspInformation.get_Type
---

# ICspInformation::get_Type


## -description

The <b>Type</b> property retrieves the type of the provider. This property is web enabled.

This property is read-only.

## -parameters

## -remarks

The values associated with the providers distributed by Microsoft are listed in the following table. Some of these providers may not be included on all operating systems and others may be included instead.

<table>
<tr>
<th>Provider</th>
<th>Type value</th>
</tr>
<tr>
<td>Microsoft Software Key Storage Provider</td>
<td>XCN_PROV_NONE (0)</td>
</tr>
<tr>
<td>Microsoft Smart Card Key Storage Provider</td>
<td>XCN_PROV_NONE (0)</td>
</tr>
<tr>
<td>Microsoft Base Cryptographic Provider v1.0</td>
<td>XCN_PROV_RSA_FULL (1)</td>
</tr>
<tr>
<td>Microsoft Base DSS and Diffie-Hellman Cryptographic Provider</td>
<td>XCN_PROV_DSS_DH (13)</td>
</tr>
<tr>
<td>Microsoft Base DSS Cryptographic Provider</td>
<td>XCN_PROV_DSS (3)</td>
</tr>
<tr>
<td>Microsoft Base Smart Card Crypto Provider</td>
<td>XCN_PROV_RSA_FULL (1)</td>
</tr>
<tr>
<td>Microsoft DH Schannel Cryptographic Provider</td>
<td>XCN_PROV_DH_SCHANNEL  (18)</td>
</tr>
<tr>
<td>Microsoft Enhanced Cryptographic Provider v1.0</td>
<td>XCN_PROV_RSA_FULL (1)</td>
</tr>
<tr>
<td>Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider</td>
<td>XCN_PROV_DSS_DH (13)</td>
</tr>
<tr>
<td>Microsoft Enhanced RSA and AES Cryptographic Provider</td>
<td>XCN_PROV_RSA_AES (24)</td>
</tr>
<tr>
<td>Microsoft RSA Schannel Cryptographic Provider</td>
<td>XCN_PROV_RSA_SCHANNEL (12)</td>
</tr>
<tr>
<td>Microsoft Strong Cryptographic Provider</td>
<td>CN_PROV_RSA_FULL (1)</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>