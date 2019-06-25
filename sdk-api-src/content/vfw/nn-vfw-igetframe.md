---
UID: NN:vfw.IGetFrame
title: IGetFrame (vfw.h)
author: windows-sdk-content
description: The IGetFrame interface supports extracting, decompressing, and displaying individual frames from an open stream.
old-location: multimedia\igetframe.htm
tech.root: Multimedia
ms.assetid: d72349bc-5e7c-4c60-b8e0-0524d02c0583
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGetFrame, IGetFrame interface [Windows Multimedia], IGetFrame interface [Windows Multimedia],described, _win32_IGetFrame, multimedia.igetframe, vfw/IGetFrame
ms.topic: interface
f1_keywords: ["vfw/IGetFrame"]
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
 - IGetFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGetFrame interface


## -description


The <b>IGetFrame</b> interface supports extracting, decompressing, and displaying individual frames from an open stream. Uses <a href="https://docs.microsoft.com/previous-versions/dd757101(v=vs.85)">IUnknown::QueryInterface</a>, <a href="https://docs.microsoft.com/previous-versions/dd757100(v=vs.85)">IUnknown::AddRef</a>, <a href="https://docs.microsoft.com/previous-versions/dd757102(v=vs.85)">IUnknown::Release</a> in addition to the following custom methods:


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetFrame</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGetFrame</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetFrame</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-igetframe-begin">Begin</a>
</td>
<td align="left" width="63%">
Prepares to extract and decompress copies of video frames from a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-igetframe-end">End</a>
</td>
<td align="left" width="63%">
Ends frame extraction and decompression.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-igetframe-getframe">GetFrame</a>
</td>
<td align="left" width="63%">
Retrieves a decompressed copy of a frame from a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-igetframe-setformat">SetFormat</a>
</td>
<td align="left" width="63%">
Sets the image format of the frames being extracted.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>
 

 

