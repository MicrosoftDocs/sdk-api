---
UID: NF:casetup.IMSCEPSetup.GetKeyLengthList
title: IMSCEPSetup::GetKeyLengthList (casetup.h)
description: Gets the list of key lengths supported by the specified cryptographic service provider (CSP). (IMSCEPSetup.GetKeyLengthList)
helpviewer_keywords: ["GetKeyLengthList","GetKeyLengthList method [Security]","GetKeyLengthList method [Security]","IMSCEPSetup interface","IMSCEPSetup interface [Security]","GetKeyLengthList method","IMSCEPSetup.GetKeyLengthList","IMSCEPSetup::GetKeyLengthList","casetup/IMSCEPSetup::GetKeyLengthList","security.imscepsetup_getkeylengthlist"]
old-location: security\imscepsetup_getkeylengthlist.htm
tech.root: security
ms.assetid: 992619dd-1d59-4033-b3aa-ae32dc9948c2
ms.date: 12/05/2018
ms.keywords: GetKeyLengthList, GetKeyLengthList method [Security], GetKeyLengthList method [Security],IMSCEPSetup interface, IMSCEPSetup interface [Security],GetKeyLengthList method, IMSCEPSetup.GetKeyLengthList, IMSCEPSetup::GetKeyLengthList, casetup/IMSCEPSetup::GetKeyLengthList, security.imscepsetup_getkeylengthlist
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
 - IMSCEPSetup::GetKeyLengthList
 - casetup/IMSCEPSetup::GetKeyLengthList
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
 - IMSCEPSetup.GetKeyLengthList
---

# IMSCEPSetup::GetKeyLengthList


## -description

The <b>GetKeyLengthList</b> method gets the list of <a href="/windows/desktop/SecGloss/k-gly">key lengths</a> supported by the specified <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

## -parameters

### -param bExchange [in]

A value that indicates whether the listed lengths are for an exchange key algorithm. A <b>VARIANT_TRUE</b>  value indicates exchange key lengths; otherwise, the lengths are for signing keys.

### -param bstrProviderName [in]

A string that contains the name of the CSP.

### -param pVal [out]

A pointer to a  <b>VARIANT</b> array of <b>VT_UI4</b> types that correspond to the key lengths supported by the CSP.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-imscepsetup">IMSCEPSetup</a>
