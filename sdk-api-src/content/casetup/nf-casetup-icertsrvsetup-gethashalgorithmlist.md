---
UID: NF:casetup.ICertSrvSetup.GetHashAlgorithmList
title: ICertSrvSetup::GetHashAlgorithmList (casetup.h)
description: Gets the list of hash algorithms supported by the specified cryptographic service provider (CSP) for an asymmetric signature key algorithm.
helpviewer_keywords: ["GetHashAlgorithmList","GetHashAlgorithmList method [Security]","GetHashAlgorithmList method [Security]","ICertSrvSetup interface","ICertSrvSetup interface [Security]","GetHashAlgorithmList method","ICertSrvSetup.GetHashAlgorithmList","ICertSrvSetup::GetHashAlgorithmList","casetup/ICertSrvSetup::GetHashAlgorithmList","security.icertsrvsetup_gethashalgorithmlist"]
old-location: security\icertsrvsetup_gethashalgorithmlist.htm
tech.root: security
ms.assetid: 451c240d-8df9-4f4a-ab0e-56c5252d3b50
ms.date: 12/05/2018
ms.keywords: GetHashAlgorithmList, GetHashAlgorithmList method [Security], GetHashAlgorithmList method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetHashAlgorithmList method, ICertSrvSetup.GetHashAlgorithmList, ICertSrvSetup::GetHashAlgorithmList, casetup/ICertSrvSetup::GetHashAlgorithmList, security.icertsrvsetup_gethashalgorithmlist
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertSrvSetup::GetHashAlgorithmList
 - casetup/ICertSrvSetup::GetHashAlgorithmList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.GetHashAlgorithmList
---

# ICertSrvSetup::GetHashAlgorithmList


## -description

The <b>GetHashAlgorithmList</b> method gets the list of hash algorithms supported by the specified <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) for an asymmetric signature key algorithm. This method does not change the state of the <b>CCertSrvSetup</b> object.

## -parameters

### -param bstrProviderName [in]

A string that contains the provider name. For key storage providers, this must be in the form <i>PublicKeyAlgorithmName</i>#<i>KeyStorageProviderName</i> for example "RSA#Microsoft Software Key Storage provider".

### -param pVal [out]

A pointer to a <b>VARIANT</b> array of <b>VT_BSTR</b> types, where each string represents the name of a hash algorithm supported by the CSP.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>