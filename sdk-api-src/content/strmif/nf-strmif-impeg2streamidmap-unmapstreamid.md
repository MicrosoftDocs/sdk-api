---
UID: NF:strmif.IMPEG2StreamIdMap.UnmapStreamId
title: IMPEG2StreamIdMap::UnmapStreamId (strmif.h)
author: windows-sdk-content
description: The UnmapStreamId method unmaps the Stream ID mapping created in a previous call to MapStreamId.
old-location: dshow\impeg2streamidmap_unmapstreamid.htm
tech.root: DirectShow
ms.assetid: 99e28b85-effd-4f86-b2da-ec02a05dde40
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMPEG2StreamIdMap interface [DirectShow],UnmapStreamId method, IMPEG2StreamIdMap.UnmapStreamId, IMPEG2StreamIdMap::UnmapStreamId, IMPEG2StreamIdMapUnmapStreamId, UnmapStreamId, UnmapStreamId method [DirectShow], UnmapStreamId method [DirectShow],IMPEG2StreamIdMap interface, dshow.impeg2streamidmap_unmapstreamid, strmif/IMPEG2StreamIdMap::UnmapStreamId
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMPEG2StreamIdMap.UnmapStreamId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMPEG2StreamIdMap::UnmapStreamId


## -description



The <code>UnmapStreamId</code> method unmaps the Stream ID mapping created in a previous call to <b>MapStreamId</b>.




## -parameters




### -param culStreamId [in]

The number of elements in the <i>pulStreamID</i> array.


### -param pulStreamId [in]

Array of Stream IDs mapped for this pin.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



There is typically only one stream ID mapped to a given pin, therefore <i>pulStreamID</i> will typically contain a single element.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/714c6b0e-3885-4026-8a83-06b37cc97d7c">IMPEG2StreamIdMap Interface</a>
 

 

