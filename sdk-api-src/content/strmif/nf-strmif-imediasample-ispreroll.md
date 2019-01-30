---
UID: NF:strmif.IMediaSample.IsPreroll
title: IMediaSample::IsPreroll
author: windows-sdk-content
description: The IsPreroll method determines if this sample is a preroll sample. A preroll sample should not be displayed.
old-location: dshow\imediasample_ispreroll.htm
tech.root: DirectShow
ms.assetid: 7df1d34f-ba55-42bd-b61b-272ef72e13a8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaSample interface [DirectShow],IsPreroll method, IMediaSample.IsPreroll, IMediaSample::IsPreroll, IMediaSampleIsPreroll, IsPreroll, IsPreroll method [DirectShow], IsPreroll method [DirectShow],IMediaSample interface, dshow.imediasample_ispreroll, strmif/IMediaSample::IsPreroll
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
 - IMediaSample.IsPreroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSample::IsPreroll


## -description



The <code>IsPreroll</code> method determines if this sample is a preroll sample. A preroll sample should not be displayed.




## -parameters






## -returns



Returns S_OK if the sample is a preroll sample. Otherwise, returns S_FALSE.




## -remarks



Preroll samples are processed but not displayed. They are located in the media stream before the displayable samples.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>
 

 

