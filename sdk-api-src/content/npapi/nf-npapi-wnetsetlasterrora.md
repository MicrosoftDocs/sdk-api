---
UID: NF:npapi.WNetSetLastErrorA
title: WNetSetLastErrorA function
author: windows-sdk-content
description: Sets extended error information. Network providers should call this function instead of SetLastError.
old-location: security\wnetsetlasterror.htm
tech.root: secauthn
ms.assetid: ee472f01-de44-4c47-9ae5-8bbac74de78b
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: WNetSetLastError, WNetSetLastError function [Security], WNetSetLastErrorA, _mnp_wnetsetlasterror, npapi/WNetSetLastError, npapi/WNetSetLastErrorA, security.wnetsetlasterror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WNetSetLastErrorA function


## -description


Sets extended error information. Network providers should call this function instead of 
<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>.

When necessary, the <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Multiple Provider Router</a> (MPR) calls <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set the Windows error returned from a network provider.
			


## -parameters




### -param err [in]

The error that occurred. This is a network-specific error code.


### -param lpError [in]

String that describes the network-specific error.


### -param lpProviders [in]

String that names the network provider that raised the error.


## -returns



This function does not return a value.




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

Providers do not need to call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> before returning from a provider function. The MPR calls <b>SetLastError</b> to set the Windows error returned from a provider when necessary to satisfy applications.



