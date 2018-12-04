---
UID: NF:mfidl.IMFByteStreamCacheControl2.SetCacheLimit
title: IMFByteStreamCacheControl2::SetCacheLimit
author: windows-sdk-content
description: Limits the cache size.
old-location: mf\imfbytestreamcachecontrol2_setcachelimit.htm
tech.root: medfound
ms.assetid: 1DDC3D76-E28B-4B8C-B2CD-FE77E840D949
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IMFByteStreamCacheControl2 interface [Media Foundation],SetCacheLimit method, IMFByteStreamCacheControl2.SetCacheLimit, IMFByteStreamCacheControl2::SetCacheLimit, SetCacheLimit, SetCacheLimit method [Media Foundation], SetCacheLimit method [Media Foundation],IMFByteStreamCacheControl2 interface, mf.imfbytestreamcachecontrol2_setcachelimit, mfidl/IMFByteStreamCacheControl2::SetCacheLimit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFByteStreamCacheControl2.SetCacheLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStreamCacheControl2::SetCacheLimit


## -description


Limits the cache size.


## -parameters




### -param qwBytes [in]

The maximum number of bytes to store in the cache, or <b>ULONGLONG_MAX </b> for no limit.  The default value is no limit.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A901F679-B6F2-4DB7-8EFC-EA61249B64FB">IMFByteStreamCacheControl2</a>
 

 

