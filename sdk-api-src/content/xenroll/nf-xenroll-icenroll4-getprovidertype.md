---
UID: NF:xenroll.ICEnroll4.getProviderType
title: ICEnroll4::getProviderType (xenroll.h)
description: Retrieves the type of the specified cryptographic service provider (CSP). This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","getProviderType method","ICEnroll4 interface [Security]","getProviderType method","ICEnroll4.getProviderType","ICEnroll4::getProviderType","getProviderType","getProviderType method [Security]","getProviderType method [Security]","CEnroll object","getProviderType method [Security]","ICEnroll4 interface","security.icenroll4_getprovidertype","xenroll/ICEnroll4::getProviderType"]
old-location: security\icenroll4_getprovidertype.htm
tech.root: security
ms.assetid: f47c07b8-0919-44d4-b331-e062341aa050
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],getProviderType method, ICEnroll4 interface [Security],getProviderType method, ICEnroll4.getProviderType, ICEnroll4::getProviderType, getProviderType, getProviderType method [Security], getProviderType method [Security],CEnroll object, getProviderType method [Security],ICEnroll4 interface, security.icenroll4_getprovidertype, xenroll/ICEnroll4::getProviderType
req.header: xenroll.h
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICEnroll4::getProviderType
 - xenroll/ICEnroll4::getProviderType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.getProviderType
 - CEnroll.getProviderType
---

# ICEnroll4::getProviderType


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getProviderType</b> method  retrieves the type of the specified <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param strProvName [in]

A string value that specifies the name of the CSP whose type is being requested.

### -param plProvType [out]

A pointer to <b>LONG</b> value that receives the CSP type. The CSP type is one of the following values.

<ul>
<li>PROV_DH_SCHANNEL</li>
<li>PROV_DSS</li>
<li>PROV_DSS_DH</li>
<li>PROV_FORTEZZA</li>
<li>PROV_MS_EXCHANGE</li>
<li>PROV_RSA_FULL</li>
<li>PROV_RSA_SCHANNEL</li>
<li>PROV_RSA_SIG</li>
<li>PROV_SSL</li>
</ul>

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 A value that represents the provider type for the provider specified by <i>strProvName</i>. This can be one of the following values.<ul>
<li>PROV_RSA_FULL</li>
<li>PROV_RSA_SIG</li>
<li>PROV_DSS</li>
<li>PROV_FORTEZZA</li>
<li>PROV_MS_EXCHANGE</li>
<li>PROV_SSL</li>
<li>PROV_RSA_SCHANNEL</li>
<li>PROV_DSS_DH</li>
<li>PROV_DH_SCHANNEL</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>