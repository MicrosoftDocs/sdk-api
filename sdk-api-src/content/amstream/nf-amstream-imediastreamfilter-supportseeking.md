---
UID: NF:amstream.IMediaStreamFilter.SupportSeeking
title: IMediaStreamFilter::SupportSeeking
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The SupportSeeking method initializes the filter to support seeking. The multimedia stream object calls this method.
old-location: dshow\imediastreamfilter_supportseeking.htm
tech.root: DirectShow
ms.assetid: 7cb15898-8a22-4621-a6e5-bb5d17640749
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IMediaStreamFilter interface [DirectShow],SupportSeeking method, IMediaStreamFilter.SupportSeeking, IMediaStreamFilter::SupportSeeking, IMediaStreamFilterSupportSeeking, SupportSeeking, SupportSeeking method [DirectShow], SupportSeeking method [DirectShow],IMediaStreamFilter interface, amstream/IMediaStreamFilter::SupportSeeking, dshow.imediastreamfilter_supportseeking
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
 - IMediaStreamFilter.SupportSeeking
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaStreamFilter::SupportSeeking


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SupportSeeking</code> method initializes the filter to support seeking. The multimedia stream object calls this method.




## -parameters




### -param bRenderer [in]

Boolean value that specifies whether the streams are being rendered. Use the value <b>TRUE</b> if the stream type is STREAMTYPE_READ, or <b>FALSE</b> otherwise.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The graph does not contain any seekable streams.

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




<a href="https://msdn.microsoft.com/1ac4976b-7088-47ac-9689-58c143746f05">IMediaStreamFilter Interface</a>
 

 

