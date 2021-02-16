---
UID: NF:casetup.IMSCEPSetup.GetProviderNameList
title: IMSCEPSetup::GetProviderNameList (casetup.h)
description: Gets the list of cryptographic service providers (CSPs) that provide asymmetric key signature and exchange algorithms on the computer.
helpviewer_keywords: ["GetProviderNameList","GetProviderNameList method [Security]","GetProviderNameList method [Security]","IMSCEPSetup interface","IMSCEPSetup interface [Security]","GetProviderNameList method","IMSCEPSetup.GetProviderNameList","IMSCEPSetup::GetProviderNameList","casetup/IMSCEPSetup::GetProviderNameList","security.imscepsetup_getprovidernamelist"]
old-location: security\imscepsetup_getprovidernamelist.htm
tech.root: security
ms.assetid: e2b5bae3-fc85-4277-8ee9-3911dacf3302
ms.date: 12/05/2018
ms.keywords: GetProviderNameList, GetProviderNameList method [Security], GetProviderNameList method [Security],IMSCEPSetup interface, IMSCEPSetup interface [Security],GetProviderNameList method, IMSCEPSetup.GetProviderNameList, IMSCEPSetup::GetProviderNameList, casetup/IMSCEPSetup::GetProviderNameList, security.imscepsetup_getprovidernamelist
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
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
 - IMSCEPSetup::GetProviderNameList
 - casetup/IMSCEPSetup::GetProviderNameList
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
 - IMSCEPSetup.GetProviderNameList
---

# IMSCEPSetup::GetProviderNameList


## -description

The <b>GetProviderNameList</b> method gets the list of <a href="/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> (CSPs) that provide asymmetric key signature and exchange algorithms on the computer.

## -parameters

### -param bExchange [in]

A value that indicates whether the provider names are for exchange key algorithms. A <b>VARIANT_TRUE</b>  value indicates exchange key providers; otherwise, the providers are for signing keys.

### -param pVal [out]

A pointer to a <b>VARIANT</b>  array of <b>VT_BSTR</b> types, where each string represents the name of a CSP.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-imscepsetup">IMSCEPSetup</a>