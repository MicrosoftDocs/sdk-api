---
UID: NF:strmif.IMediaSample.GetPointer
title: IMediaSample::GetPointer (strmif.h)
author: windows-sdk-content
description: The GetPointer method retrieves a read/write pointer to the media sample's buffer.
old-location: dshow\imediasample_getpointer.htm
tech.root: DirectShow
ms.assetid: a3c69dfb-6ee4-401b-8dcb-4e42a8cd8156
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPointer, GetPointer method [DirectShow], GetPointer method [DirectShow],IMediaSample interface, IMediaSample interface [DirectShow],GetPointer method, IMediaSample.GetPointer, IMediaSample::GetPointer, IMediaSampleGetPointer, dshow.imediasample_getpointer, strmif/IMediaSample::GetPointer
ms.topic: method
f1_keywords: 
 - "strmif/IMediaSample.GetPointer"
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
 - IMediaSample.GetPointer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSample::GetPointer


## -description



The <code>GetPointer</code> method retrieves a read/write pointer to the media sample's buffer.




## -parameters




### -param ppBuffer [out]

Receives a pointer to the buffer.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



The buffer memory is owned by the media sample object, and is automatically released when the media sample is destroyed. The caller should not free or reallocate the buffer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>
 

 

