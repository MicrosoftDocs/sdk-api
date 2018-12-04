---
UID: NF:amstream.IAMMediaTypeStream.SetFormat
title: IAMMediaTypeStream::SetFormat
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The SetFormat method sets the format of the stream.
old-location: dshow\iammediatypestream_setformat.htm
tech.root: DirectShow
ms.assetid: 12ac4490-c12c-428a-939f-adf25a77b9e4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IAMMediaTypeStream interface [DirectShow],SetFormat method, IAMMediaTypeStream.SetFormat, IAMMediaTypeStream::SetFormat, IAMMediaTypeStreamSetFormat, SetFormat, SetFormat method [DirectShow], SetFormat method [DirectShow],IAMMediaTypeStream interface, amstream/IAMMediaTypeStream::SetFormat, dshow.iammediatypestream_setformat
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeStream.SetFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaTypeStream::SetFormat


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetFormat</code> method sets the format of the stream.




## -parameters




### -param pMediaType [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that contains the stream format.


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
<dt><b>MS_E_SAMPLEALLOC</b></dt>
</dl>
</td>
<td width="60%">
The stream has already allocated a sample with another media type.

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
 

 

