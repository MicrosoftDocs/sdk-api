---
UID: NC:wincrypt.PFN_CERT_ENUM_SYSTEM_STORE_LOCATION
title: PFN_CERT_ENUM_SYSTEM_STORE_LOCATION (wincrypt.h)
description: The CertEnumSystemStoreLocationCallback callback function formats and presents information on each system store location found by a call to CertEnumSystemStoreLocation.
helpviewer_keywords: ["CertEnumSystemStoreLocationCallback","CertEnumSystemStoreLocationCallback callback function [Security]","PFN_CERT_ENUM_SYSTEM_STORE_LOCATION","PFN_CERT_ENUM_SYSTEM_STORE_LOCATION callback","security.certenumsystemstorelocationcallback","wincrypt/CertEnumSystemStoreLocationCallback"]
old-location: security\certenumsystemstorelocationcallback.htm
tech.root: security
ms.assetid: a5f1badd-3e68-4e0f-9a42-1b1876c9cb56
ms.date: 12/05/2018
ms.keywords: CertEnumSystemStoreLocationCallback, CertEnumSystemStoreLocationCallback callback function [Security], PFN_CERT_ENUM_SYSTEM_STORE_LOCATION, PFN_CERT_ENUM_SYSTEM_STORE_LOCATION callback, security.certenumsystemstorelocationcallback, wincrypt/CertEnumSystemStoreLocationCallback
req.header: wincrypt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CERT_ENUM_SYSTEM_STORE_LOCATION
 - wincrypt/PFN_CERT_ENUM_SYSTEM_STORE_LOCATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - CertEnumSystemStoreLocationCallback
---

# PFN_CERT_ENUM_SYSTEM_STORE_LOCATION callback function


## -description

The <b>CertEnumSystemStoreLocationCallback</b> 
	callback function formats and presents information on each system store location found by a call to 
	<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstorelocation">CertEnumSystemStoreLocation</a>.

## -parameters

### -param pwszStoreLocation [in]

String that contains information on the store location found.

### -param dwFlags [in]

Flag used to call for an alteration of the presentation.

### -param pvReserved [in]

Reserved for future use.

### -param pvArg [in]

A pointer to information passed to the callback function in the <i>pvArg</i> 
	 passed to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsystemstorelocation">CertEnumSystemStoreLocation</a>.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.
