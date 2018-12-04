---
UID: NF:strmif.IMediaSeeking.GetDuration
title: IMediaSeeking::GetDuration
author: windows-sdk-content
description: The GetDuration method gets the duration of the stream.
old-location: dshow\imediaseeking_getduration.htm
tech.root: DirectShow
ms.assetid: 15b98fb0-a0dd-47fc-8046-fa336afa970c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetDuration, GetDuration method [DirectShow], GetDuration method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetDuration method, IMediaSeeking.GetDuration, IMediaSeeking::GetDuration, IMediaSeekingGetDuration, dshow.imediaseeking_getduration, strmif/IMediaSeeking::GetDuration
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
 - IMediaSeeking.GetDuration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSeeking::GetDuration


## -description


The <b>GetDuration</b> method gets the duration of the stream.


## -parameters




### -param pDuration [out]

Receives the duration, in units of the current time format.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method gets the duration of the stream at normal playback speed. Changing the playback rate does not affect the duration.
      

The duration is expressed in the current time format. The default time format is <a href="https://msdn.microsoft.com/862c95bc-2e0a-42c0-b907-45f64f27bd41">REFERENCE_TIME</a> units (100 nanoseconds). To change time formats, use the <a href="https://msdn.microsoft.com/b6f64f8a-67b8-4297-8f0d-389001fa1681">IMediaSeeking::SetTimeFormat</a> method.
      

Depending on the source format, the duration might not be exact. For example, if the source contains a variable bit-rate (VBR) stream, the method might return an estimated duration.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking Interface</a>
 

 

