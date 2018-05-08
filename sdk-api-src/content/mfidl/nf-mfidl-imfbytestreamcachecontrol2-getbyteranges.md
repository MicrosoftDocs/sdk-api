---
UID: NF:mfidl.IMFByteStreamCacheControl2.GetByteRanges
title: IMFByteStreamCacheControl2::GetByteRanges
author: windows-driver-content
description: Gets the ranges of bytes that are currently stored in the cache.
old-location: mf\imfbytestreamcachecontrol2_getbyteranges.htm
old-project: medfound
ms.assetid: FC91FCB5-CD22-494F-85B7-38571C38A44E
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetByteRanges, GetByteRanges method [Media Foundation], GetByteRanges method [Media Foundation],IMFByteStreamCacheControl2 interface, IMFByteStreamCacheControl2 interface [Media Foundation],GetByteRanges method, IMFByteStreamCacheControl2.GetByteRanges, IMFByteStreamCacheControl2::GetByteRanges, mf.imfbytestreamcachecontrol2_getbyteranges, mfidl/IMFByteStreamCacheControl2::GetByteRanges
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFByteStreamCacheControl2.GetByteRanges
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamCacheControl2::GetByteRanges


## -description


Gets the ranges of bytes that are currently stored in the cache.


## -parameters




### -param pcRanges [out]

Receives the number of ranges returned in the <i>ppRanges</i> array.


### -param ppRanges [out]

Receives an array of <a href="https://msdn.microsoft.com/BE684626-32AC-4BF1-8CF1-D68F8A0ABB9E">MF_BYTE_STREAM_CACHE_RANGE</a> structures. Each structure specifies a range of bytes stored in the cache. The caller must free the array by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A901F679-B6F2-4DB7-8EFC-EA61249B64FB">IMFByteStreamCacheControl2</a>
 

 

