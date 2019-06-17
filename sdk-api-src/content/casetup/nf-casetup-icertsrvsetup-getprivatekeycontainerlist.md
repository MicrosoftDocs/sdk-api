---
UID: NF:casetup.ICertSrvSetup.GetPrivateKeyContainerList
title: ICertSrvSetup::GetPrivateKeyContainerList (casetup.h)
author: windows-sdk-content
description: Gets the list of key container names stored by the specified cryptographic service provider (CSP) for asymmetric signature key algorithms.
old-location: security\icertsrvsetup_getprivatekeycontainerlist.htm
tech.root: SecCrypto
ms.assetid: a57590d3-0882-4407-b920-964c0e489f80
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPrivateKeyContainerList, GetPrivateKeyContainerList method [Security], GetPrivateKeyContainerList method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetPrivateKeyContainerList method, ICertSrvSetup.GetPrivateKeyContainerList, ICertSrvSetup::GetPrivateKeyContainerList, casetup/ICertSrvSetup::GetPrivateKeyContainerList, security.icertsrvsetup_getprivatekeycontainerlist
ms.topic: method
f1_keywords: ["casetup/ICertSrvSetup.GetPrivateKeyContainerList"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.GetPrivateKeyContainerList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertSrvSetup::GetPrivateKeyContainerList


## -description


The <b>GetPrivateKeyContainerList</b> method gets the list of <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">key container</a> names stored by the specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) for asymmetric signature key algorithms. This method does not change the state of the <b>CCertSrvSetup</b> object.


## -parameters




### -param bstrProviderName [in]

A string that contains the name of the provider. For key storage providers, this must be in the form <i>PublicKeyAlgorithmName</i>#<i>KeyStorageProviderName</i> for example "RSA#Microsoft Software Key Storage provider".


### -param pVal [out]

A pointer to a <b>VARIANT</b> array of <b>VT_BSTR</b> types, where each string represents the name of a key container used by the specified CSP.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>
 

 

