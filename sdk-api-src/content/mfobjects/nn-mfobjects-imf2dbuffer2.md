---
UID: NN:mfobjects.IMF2DBuffer2
title: IMF2DBuffer2
author: windows-sdk-content
description: Represents a buffer that contains a two-dimensional surface, such as a video frame.
old-location: mf\imf2dbuffer2.htm
tech.root: medfound
ms.assetid: BFA73B1A-F8A7-4100-9DBD-234CCA06F9F5
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMF2DBuffer2, IMF2DBuffer2 interface [Media Foundation], IMF2DBuffer2 interface [Media Foundation],described, mf.imf2dbuffer2, mfobjects/IMF2DBuffer2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfobjects.h
api_name:
 - IMF2DBuffer2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMF2DBuffer2 interface


## -description


Represents a buffer that contains a two-dimensional surface, such as a video frame.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMF2DBuffer2</b> interface inherits from <a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a>. <b>IMF2DBuffer2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMF2DBuffer2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90B0CBA2-2474-4B34-8BB4-6C59C05CDD7E">Copy2DTo</a>
</td>
<td align="left" width="63%">
Copies the buffer to another 2D buffer object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84885FEF-7F6D-4BE3-BF63-F9EC0C7E2D88">Lock2DSize</a>
</td>
<td align="left" width="63%">
Gives the caller access to the memory in the buffer.

</td>
</tr>
</table> 


## -remarks



This interface extends the <a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a> interface and adds a safer version of the <a href="https://msdn.microsoft.com/887a7394-9fe0-473a-825b-f095b01626c4">IMF2DBuffer::Lock2D</a> method.




## -see-also




<a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a>



<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/be5ec8a8-2d0b-401b-9d05-fdb87ad8c864">Uncompressed Video Buffers</a>
 

 

