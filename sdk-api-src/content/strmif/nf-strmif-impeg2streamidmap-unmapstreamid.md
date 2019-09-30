---
UID: NF:strmif.IMPEG2StreamIdMap.UnmapStreamId
title: IMPEG2StreamIdMap::UnmapStreamId (strmif.h)
author: windows-sdk-content
description: The UnmapStreamId method unmaps the Stream ID mapping created in a previous call to MapStreamId.
old-location: dshow\impeg2streamidmap_unmapstreamid.htm
tech.root: DirectShow
ms.assetid: 99e28b85-effd-4f86-b2da-ec02a05dde40
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMPEG2StreamIdMap interface [DirectShow],UnmapStreamId method, IMPEG2StreamIdMap.UnmapStreamId, IMPEG2StreamIdMap::UnmapStreamId, IMPEG2StreamIdMapUnmapStreamId, UnmapStreamId, UnmapStreamId method [DirectShow], UnmapStreamId method [DirectShow],IMPEG2StreamIdMap interface, dshow.impeg2streamidmap_unmapstreamid, strmif/IMPEG2StreamIdMap::UnmapStreamId
ms.topic: method
f1_keywords: 
 - "strmif/IMPEG2StreamIdMap.UnmapStreamId"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-impeg2streamidmap">IMPEG2StreamIdMap Interface</a>
 

 

