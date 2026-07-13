---
UID: NF:npapi.WNetSetLastErrorA
title: WNetSetLastErrorA function (npapi.h)
description: Sets extended error information. Network providers should call this function instead of SetLastError. (ANSI)
helpviewer_keywords: ["WNetSetLastErrorA", "npapi/WNetSetLastErrorA"]
old-location: security\wnetsetlasterror.htm
tech.root: security
ms.assetid: ee472f01-de44-4c47-9ae5-8bbac74de78b
ms.date: 12/05/2018
ms.keywords: WNetSetLastError, WNetSetLastError function [Security], WNetSetLastErrorA, _mnp_wnetsetlasterror, npapi/WNetSetLastError, npapi/WNetSetLastErrorA, security.wnetsetlasterror
req.header: npapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetSetLastErrorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WNetSetLastErrorA
 - npapi/WNetSetLastErrorA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
api_name:
 - WNetSetLastError
 - WNetSetLastErrorA
---

# WNetSetLastErrorA function


## -description

Sets extended error information. Network providers should call this function instead of 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a>.

When necessary, the <a href="/windows/desktop/SecGloss/m-gly">Multiple Provider Router</a> (MPR) calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> to set the Windows error returned from a network provider.

## -parameters

### -param err [in]

The error that occurred. This is a network-specific error code.

### -param lpError [in]

String that describes the network-specific error.

### -param lpProviders [in]

String that names the network provider that raised the error.

## -remarks

This function is implemented by the Windows operating system and can be called by network providers.

A provider should use this function to report errors that contain provider-specific information. The error information is saved until it is overwritten by another call to <b>WNetSetLastError</b> in the same thread.

The recommended way for a provider function to handle general errors is to use the following statement.


```cpp
return(providerError);

```


In this statement, providerError is a Windows error code, such as one of the return codes listed for the provider API in this document.

For provider-specific errors, a provider should do the following.


```cpp
//  Set up lpErrorString to be the error to be reported.
WNetSetLastError(providerError,
lpErrorString,
lpProviderName) ;
return(ERROR_EXTENDED_ERROR) ;

```


In this case, providerError is the provider-specific error code.

Providers do not need to call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> before returning from a provider function. The MPR calls <b>SetLastError</b> to set the Windows error returned from a provider when necessary to satisfy applications.
