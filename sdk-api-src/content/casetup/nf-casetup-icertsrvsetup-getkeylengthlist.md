---
UID: NF:casetup.ICertSrvSetup.GetKeyLengthList
title: ICertSrvSetup::GetKeyLengthList (casetup.h)
description: Gets the list of key lengths supported by the specified cryptographic service provider (CSP). (ICertSrvSetup.GetKeyLengthList)
helpviewer_keywords: ["GetKeyLengthList","GetKeyLengthList method [Security]","GetKeyLengthList method [Security]","ICertSrvSetup interface","ICertSrvSetup interface [Security]","GetKeyLengthList method","ICertSrvSetup.GetKeyLengthList","ICertSrvSetup::GetKeyLengthList","casetup/ICertSrvSetup::GetKeyLengthList","security.icertsrvsetup_getkeylengthlist"]
old-location: security\icertsrvsetup_getkeylengthlist.htm
tech.root: security
ms.assetid: 9360522a-05fd-41ae-95b1-9270a9f4f728
ms.date: 12/05/2018
ms.keywords: GetKeyLengthList, GetKeyLengthList method [Security], GetKeyLengthList method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetKeyLengthList method, ICertSrvSetup.GetKeyLengthList, ICertSrvSetup::GetKeyLengthList, casetup/ICertSrvSetup::GetKeyLengthList, security.icertsrvsetup_getkeylengthlist
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
 - ICertSrvSetup::GetKeyLengthList
 - casetup/ICertSrvSetup::GetKeyLengthList
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
 - ICertSrvSetup.GetKeyLengthList
---

# ICertSrvSetup::GetKeyLengthList


## -description

The <b>GetKeyLengthList</b> method gets the list of <a href="/windows/desktop/SecGloss/k-gly">key lengths</a> supported by the specified <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). This method does not change the state of the <b>CCertSrvSetup</b> object.

## -parameters

### -param bstrProviderName [in]

A string that contains the name of the provider. For key storage providers, this must be in the form <i>PublicKeyAlgorithmName</i>#<i>KeyStorageProviderName</i> for example "RSA#Microsoft Software Key Storage provider".

### -param pVal [out]

A pointer to a <b>VARIANT</b> array of <b>VT_UI4</b> types that correspond to the key lengths supported by the CSP.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>
