---
UID: NN:vfw.IAVIStream
title: IAVIStream (vfw.h)
author: windows-sdk-content
description: The IAVIStream interface supports creating and manipulating data streams within a file. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:\_
The IAVIStream interface supports creating and manipulating data streams within a file. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:
old-location: multimedia\iavistream.htm
tech.root: Multimedia
ms.assetid: 25f67f04-e005-48ee-89e7-a6ef89f6d6c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAVIStream, IAVIStream interface [Windows Multimedia], IAVIStream interface [Windows Multimedia],described, _win32_IAVIStream, multimedia.iavistream, vfw/IAVIStream
ms.topic: interface
f1_keywords: ["vfw/IAVIStream"]
req.header: vfw.h
req.include-header: 
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
req.lib: Vfw32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IAVIStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAVIStream interface


## -description



The <b>IAVIStream</b> interface supports creating and manipulating data streams within a file. Uses <a href="https://docs.microsoft.com/previous-versions/dd757101(v=vs.85)">IUnknown::QueryInterface</a>, <a href="https://docs.microsoft.com/previous-versions/dd757100(v=vs.85)">IUnknown::AddRef</a>, <a href="https://docs.microsoft.com/previous-versions/dd757102(v=vs.85)">IUnknown::Release</a> in addition to the following custom methods:




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAVIStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAVIStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAVIStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistream-create">Create</a>
</td>
<td align="left" width="63%">
Initializes a stream handler that is not associated with any file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistream-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes data from a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistream-findsample">FindSample</a>
</td>
<td align="left" width="63%">
Obtains the position in a stream of a key frame or a nonempty frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistream-info">Info</a>
</td>
<td align="left" width="63%">
Fills and returns an <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-_avistreaminfoa">AVISTREAMINFO</a> structure with information about a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistream-read">Read</a>
</td>
<td align="left" width="63%">
Reads data from a stream and copies it to an application-defined buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistream-readdata">ReadData</a>
</td>
<td align="left" width="63%">
Reads data headers, format data, or nonaudio and nonvideo data. (Use the Read method to read audio and video data.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistream-readformat">ReadFormat</a>
</td>
<td align="left" width="63%">
Obtains format information from a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistream-setformat">SetFormat</a>
</td>
<td align="left" width="63%">
Sets format information in a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistream-write">Write</a>
</td>
<td align="left" width="63%">
Writes data to a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistream-writedata">WriteData</a>
</td>
<td align="left" width="63%">
Writes data headers, format data, or nonaudio and nonvideo data. (Use the <b>Write</b> method to write audio and video data.)

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>
 

 

