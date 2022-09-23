---
UID: NF:npapi.WNetSetLastErrorW
tech.root: security 
title: WNetSetLastErrorW
ms.date: 04/14/2021
targetos: Windows
description: Sets extended error information. Network providers should call this function instead of SetLastError. (Unicode)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Mpr.dll
req.header: npapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mpr.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps only] 
req.target-min-winversvr: Windows Server 2003 [desktop apps only] 
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Mpr.dll
api_name:
 - WNetSetLastErrorW
 - WNetSetLastError
f1_keywords:
 - WNetSetLastErrorW
 - npapi/WNetSetLastErrorW
 - WNetSetLastError
 - npapi/WNetSetLastError
dev_langs:
 - c++
---

# WNetSetLastErrorW function

## -description

Sets extended error information. Network providers should call this function instead of <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a>.

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
lpProviderName);
return(ERROR_EXTENDED_ERROR);
```

In this case, providerError is the provider-specific error code.

Providers do not need to call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> before returning from a provider function. The MPR calls <b>SetLastError</b> to set the Windows error returned from a provider when necessary to satisfy applications.
