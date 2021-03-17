---
UID: NF:wintrust.WintrustAddDefaultForUsage
title: WintrustAddDefaultForUsage function (wintrust.h)
description: Specifies the default usage identifier and callback information for a provider.
helpviewer_keywords: ["WintrustAddDefaultForUsage","WintrustAddDefaultForUsage function [Security]","security.wintrustadddefaultforusage","wintrust/WintrustAddDefaultForUsage"]
old-location: security\wintrustadddefaultforusage.htm
tech.root: security
ms.assetid: 511D05BD-0F8C-45B8-A1B0-D3C7AAFECCFC
ms.date: 12/05/2018
ms.keywords: WintrustAddDefaultForUsage, WintrustAddDefaultForUsage function [Security], security.wintrustadddefaultforusage, wintrust/WintrustAddDefaultForUsage
req.header: wintrust.h
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
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WintrustAddDefaultForUsage
 - wintrust/WintrustAddDefaultForUsage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - WintrustAddDefaultForUsage
---

# WintrustAddDefaultForUsage function


## -description

The <b>WintrustAddDefaultForUsage</b> function specifies the default usage identifier and callback information for a provider.

## -parameters

### -param pszUsageOID [in]

Pointer to a string that contains the identifier.

### -param psDefUsage [in]

Pointer to a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_regdefusage">CRYPT_PROVIDER_REGDEFUSAGE</a> structure that contains callback information.

## -returns

The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b>  if the function fails.   If the function fails, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function  to determine the reason for failure.

## -remarks

If the provider uses this function and requires any of the callback data, the provider must completely fill out the <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_regdefusage">CRYPT_PROVIDER_REGDEFUSAGE</a> structure.

The usage and callback information can be retrieved by calling the <a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustgetdefaultforusage">WintrustGetDefaultForUsage</a> function.

## -see-also

<a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_defusage">CRYPT_PROVIDER_DEFUSAGE</a>



<a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_regdefusage">CRYPT_PROVIDER_REGDEFUSAGE</a>



<a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustgetdefaultforusage">WintrustGetDefaultForUsage</a>