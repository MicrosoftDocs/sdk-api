---
UID: NF:casetup.ICertSrvSetup.GetProviderNameList
title: ICertSrvSetup::GetProviderNameList (casetup.h)
description: Gets the list of cryptographic service providers (CSPs) that provide asymmetric key signature algorithms on the computer.
helpviewer_keywords: ["GetProviderNameList","GetProviderNameList method [Security]","GetProviderNameList method [Security]","ICertSrvSetup interface","ICertSrvSetup interface [Security]","GetProviderNameList method","ICertSrvSetup.GetProviderNameList","ICertSrvSetup::GetProviderNameList","casetup/ICertSrvSetup::GetProviderNameList","security.icertsrvsetup_getprovidernamelist"]
old-location: security\icertsrvsetup_getprovidernamelist.htm
tech.root: security
ms.assetid: a0915981-8023-4ce8-a870-7acc75c574ac
ms.date: 12/05/2018
ms.keywords: GetProviderNameList, GetProviderNameList method [Security], GetProviderNameList method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetProviderNameList method, ICertSrvSetup.GetProviderNameList, ICertSrvSetup::GetProviderNameList, casetup/ICertSrvSetup::GetProviderNameList, security.icertsrvsetup_getprovidernamelist
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
 - ICertSrvSetup::GetProviderNameList
 - casetup/ICertSrvSetup::GetProviderNameList
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
 - ICertSrvSetup.GetProviderNameList
---

# ICertSrvSetup::GetProviderNameList


## -description

The <b>GetProviderNameList</b> method gets the list of <a href="/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> (CSPs) that provide asymmetric key signature algorithms on the computer. This method does not change the state of the <b>CCertSrvSetup</b> object.

## -parameters

### -param pVal [out]

A pointer to a <b>VARIANT</b> array of <b>VT_BSTR</b> types, where each string represents the name of a CSP.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>