---
UID: NF:strmif.IMediaSample.SetMediaTime
title: IMediaSample::SetMediaTime
author: windows-sdk-content
description: The SetMediaTime method sets the media times for this sample.
old-location: dshow\imediasample_setmediatime.htm
tech.root: DirectShow
ms.assetid: 8ae9db99-828d-4ac9-aa51-668b84d4dfab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaSample interface [DirectShow],SetMediaTime method, IMediaSample.SetMediaTime, IMediaSample::SetMediaTime, IMediaSampleSetMediaTime, SetMediaTime, SetMediaTime method [DirectShow], SetMediaTime method [DirectShow],IMediaSample interface, dshow.imediasample_setmediatime, strmif/IMediaSample::SetMediaTime
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
 - IMediaSample.SetMediaTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSample::SetMediaTime


## -description



The <code>SetMediaTime</code> method sets the media times for this sample.




## -parameters




### -param pTimeStart [in]

Pointer to the beginning media time.


### -param pTimeEnd [in]

Pointer to the ending media time.


## -returns



Returns S_OK, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



To invalidate the media time, set <i>pTimeStart</i> and <i>pTimeEnd</i> to <b>NULL</b>. This will cause the <a href="https://msdn.microsoft.com/eb2a8fd4-4a25-482c-8509-f43461c708d6">IMediaSample::GetMediaTime</a> method to return VFW_E_MEDIA_TIME_NOT_SET.

For more information about media times, see <a href="https://msdn.microsoft.com/445fe6b9-9d5b-45fd-9c9e-8c632c5228ae">Time Stamps</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>
 

 

