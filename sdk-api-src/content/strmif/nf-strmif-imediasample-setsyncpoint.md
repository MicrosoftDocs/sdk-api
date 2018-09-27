---
UID: NF:strmif.IMediaSample.SetSyncPoint
title: IMediaSample::SetSyncPoint
author: windows-sdk-content
description: The SetSyncPoint method specifies whether the beginning of this sample is a synchronization point.
old-location: dshow\imediasample_setsyncpoint.htm
tech.root: DirectShow
ms.assetid: b2770045-c18b-4dbc-b104-873e07c0b5aa
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IMediaSample interface [DirectShow],SetSyncPoint method, IMediaSample.SetSyncPoint, IMediaSample::SetSyncPoint, IMediaSampleSetSyncPoint, SetSyncPoint, SetSyncPoint method [DirectShow], SetSyncPoint method [DirectShow],IMediaSample interface, dshow.imediasample_setsyncpoint, strmif/IMediaSample::SetSyncPoint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMediaSample.SetSyncPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSample::SetSyncPoint


## -description



The <code>SetSyncPoint</code> method specifies whether the beginning of this sample is a synchronization point.




## -parameters




### -param bIsSyncPoint [in]

Boolean value that specifies whether this is a synchronization point. If <b>TRUE</b>, this is a synchronization point.


## -returns



Returns S_OK or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



The filter that first generates the data in the sample should set this flag to <b>TRUE</b> or <b>FALSE</b>, as appropriate. For uncompressed video and PCM audio, set every sample to <b>TRUE</b>. For compressed video, set key frames to <b>TRUE</b> and delta frames to <b>FALSE</b>.

This flag is purely informational. Other filters downstream might check this flag; for example, a filter might need to skip to the next key frame.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>



<a href="https://msdn.microsoft.com/eed64bd9-1300-4db3-a3ed-c7e8ff9c7c8f">IMediaSample::IsSyncPoint</a>
 

 

