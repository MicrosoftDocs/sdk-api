---
UID: NF:strmif.IMediaSample.IsSyncPoint
title: IMediaSample::IsSyncPoint (strmif.h)

description: The IsSyncPoint method determines if the beginning of this sample is a synchronization point.
old-location: dshow\imediasample_issyncpoint.htm
tech.root: DirectShow
ms.assetid: eed64bd9-1300-4db3-a3ed-c7e8ff9c7c8f

ms.date: 12/05/2018
ms.keywords: IMediaSample interface [DirectShow],IsSyncPoint method, IMediaSample.IsSyncPoint, IMediaSample::IsSyncPoint, IMediaSampleIsSyncPoint, IsSyncPoint, IsSyncPoint method [DirectShow], IsSyncPoint method [DirectShow],IMediaSample interface, dshow.imediasample_issyncpoint, strmif/IMediaSample::IsSyncPoint
ms.topic: method
f1_keywords: 
 - "strmif/IMediaSample.IsSyncPoint"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IMediaSample.IsSyncPoint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSample::IsSyncPoint


## -description



The <code>IsSyncPoint</code> method determines if the beginning of this sample is a synchronization point.




## -parameters






## -returns



Returns S_OK if the sample is a synchronization point. Otherwise, returns S_FALSE.




## -remarks



A filter can begin a stream at any synchronization point. With some compression types, streaming can begin only at certain points in the stream; for example, on key frames. If the <b>bTemporalCompression</b> member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure is <b>FALSE</b>, all samples are synchronization points.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>
 

 

