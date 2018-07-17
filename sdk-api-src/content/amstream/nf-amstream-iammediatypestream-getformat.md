---
UID: NF:amstream.IAMMediaTypeStream.GetFormat
title: IAMMediaTypeStream::GetFormat
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The GetFormat method retrieves the format of the stream.
old-location: dshow\iammediatypestream_getformat.htm
old-project: DirectShow
ms.assetid: 9f00fe45-df4b-4787-980c-9fe434a8ab7e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetFormat, GetFormat method [DirectShow], GetFormat method [DirectShow],IAMMediaTypeStream interface, IAMMediaTypeStream interface [DirectShow],GetFormat method, IAMMediaTypeStream.GetFormat, IAMMediaTypeStream::GetFormat, IAMMediaTypeStreamGetFormat, amstream/IAMMediaTypeStream::GetFormat, dshow.iammediatypestream_getformat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AMSI_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeStream.GetFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAMMediaTypeStream::GetFormat


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetFormat</code> method retrieves the format of the stream.




## -parameters




### -param pMediaType [out]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that receives the stream format.


### -param dwFlags [in]

Reserved.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_NOSTREAM</b></dt>
</dl>
</td>
<td width="60%">
No stream is associated with this object.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6ca1bad2-625b-4415-8311-acd5443452c1">IAMMediaTypeStream Interface</a>
 

 

