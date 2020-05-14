---
UID: NF:certenroll.IAlternativeName.get_RawData
title: IAlternativeName::get_RawData (certenroll.h)
description: Retrieves the Distinguished Encoding Rules (DER) encoded byte array that contains the name.helpviewer_keywords: ["IAlternativeName interface [Security]","RawData property","IAlternativeName.RawData","IAlternativeName.get_RawData","IAlternativeName::RawData","IAlternativeName::get_RawData","RawData property [Security]","RawData property [Security]","IAlternativeName interface","certenroll/IAlternativeName::RawData","certenroll/IAlternativeName::get_RawData","get_RawData","security.ialternativename_rawdata_property"]
old-location: security\ialternativename_rawdata_property.htm
tech.root: seccertenroll
ms.assetid: 7385654d-03f8-4796-a95c-000fa8ab65a3
ms.date: 12/05/2018
ms.keywords: IAlternativeName interface [Security],RawData property, IAlternativeName.RawData, IAlternativeName.get_RawData, IAlternativeName::RawData, IAlternativeName::get_RawData, RawData property [Security], RawData property [Security],IAlternativeName interface, certenroll/IAlternativeName::RawData, certenroll/IAlternativeName::get_RawData, get_RawData, security.ialternativename_rawdata_property
f1_keywords:
- certenroll/IAlternativeName.RawData
dev_langs:
- c++
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
- IAlternativeName.RawData
- IAlternativeName.get_RawData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAlternativeName::get_RawData


## -description


The <b>RawData</b> property retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the name. The byte array is contained in a Unicode encoded string.

This property is read-only.


## -parameters


## -remarks



You can retrieve a value for this property if you initialized the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a> object in any of the following ways:

<ul>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromothername">InitializeFromOtherName</a> and supply an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromrawdata">InitializeFromRawData</a> and specify the XCN_CERT_ALT_NAME_GUID,  XCN_CERT_ALT_NAME_DIRECTORY_NAME, or XCN_CERT_ALT_NAME_IP_ADDRESS types.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromstring">InitializeFromString</a> and specify the XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME type.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>
 

 

