---
UID: NF:strmif.IMediaSample.SetPreroll
title: IMediaSample::SetPreroll (strmif.h)
author: windows-sdk-content
description: The SetPreroll method specifies whether this sample is a preroll sample.
old-location: dshow\imediasample_setpreroll.htm
tech.root: DirectShow
ms.assetid: a92f2774-19ac-4630-ad66-2299336d1338
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaSample interface [DirectShow],SetPreroll method, IMediaSample.SetPreroll, IMediaSample::SetPreroll, IMediaSampleSetPreroll, SetPreroll, SetPreroll method [DirectShow], SetPreroll method [DirectShow],IMediaSample interface, dshow.imediasample_setpreroll, strmif/IMediaSample::SetPreroll
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
 - IMediaSample.SetPreroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSample::SetPreroll


## -description



The <code>SetPreroll</code> method specifies whether this sample is a preroll sample.




## -parameters




### -param bIsPreroll

Boolean value that specifies whether this is a preroll sample. If <b>TRUE</b>, this is a preroll sample.


## -returns



Returns S_OK, or an <b>HRESULT</b> value indicating the cause of the error.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>



<a href="https://msdn.microsoft.com/7df1d34f-ba55-42bd-b61b-272ef72e13a8">IMediaSample::IsPreroll</a>
 

 

