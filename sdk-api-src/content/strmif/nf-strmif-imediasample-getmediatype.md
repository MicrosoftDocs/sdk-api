---
UID: NF:strmif.IMediaSample.GetMediaType
title: IMediaSample::GetMediaType
author: windows-sdk-content
description: The GetMediaType method retrieves the media type, if the media type differs from the previous sample.
old-location: dshow\imediasample_getmediatype.htm
old-project: DirectShow
ms.assetid: abccec09-c5a0-4192-9bdf-9240d1b73357
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetMediaType, GetMediaType method [DirectShow], GetMediaType method [DirectShow],IMediaSample interface, IMediaSample interface [DirectShow],GetMediaType method, IMediaSample.GetMediaType, IMediaSample::GetMediaType, IMediaSampleGetMediaType, dshow.imediasample_getmediatype, strmif/IMediaSample::GetMediaType
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaSample.GetMediaType
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaSample::GetMediaType


## -description



The <code>GetMediaType</code> method retrieves the media type, if the media type differs from the previous sample.




## -parameters




### -param ppMediaType

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure. If the media type has not changed from the previous sample, <i>*ppMediaType</i> is set to <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The media type has not changed from the previous sample.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



This method enables a filter to make limited changes to the media type, such as changing the palette. To make a significant change to the media type, the pins might need to reconnect and renegotiate the media type.

If the method returns S_OK, the caller must free the memory for the media type, including the format block. You can use the <a href="https://msdn.microsoft.com/970f6b2b-2bf5-418d-b4ae-637561cd6765">DeleteMediaType</a> function in the DirectShow base class library.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>
 

 

