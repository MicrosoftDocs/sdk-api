---
UID: NN:vfw.IGetFrame
title: IGetFrame
author: windows-sdk-content
description: The IGetFrame interface supports extracting, decompressing, and displaying individual frames from an open stream.
old-location: multimedia\igetframe.htm
tech.root: Multimedia
ms.assetid: d72349bc-5e7c-4c60-b8e0-0524d02c0583
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IGetFrame, IGetFrame interface [Windows Multimedia], IGetFrame interface [Windows Multimedia],described, _win32_IGetFrame, multimedia.igetframe, vfw/IGetFrame
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IGetFrame interface


## -description


The <b>IGetFrame</b> interface supports extracting, decompressing, and displaying individual frames from an open stream. Uses <a href="https://msdn.microsoft.com/6db0af58-51ee-499a-81c4-4bce8aae0f06">IUnknown::QueryInterface</a>, <a href="https://msdn.microsoft.com/14ffd2ab-ac0c-4de7-adb8-4fe800c9bda9">IUnknown::AddRef</a>, <a href="https://msdn.microsoft.com/61d760e3-72bf-462e-bfd5-5578b53860ba">IUnknown::Release</a> in addition to the following custom methods:


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetFrame</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGetFrame</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2d2c1872-e0c3-4fea-bfb9-45b814973072">Begin</a>
</td>
<td align="left" width="63%">
Prepares to extract and decompress copies of video frames from a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc5423c7-4f21-4941-adda-6f4665e86210">End</a>
</td>
<td align="left" width="63%">
Ends frame extraction and decompression.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2b76aad-e2db-4e04-be54-b697830e8644">GetFrame</a>
</td>
<td align="left" width="63%">
Retrieves a decompressed copy of a frame from a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96a2afa5-af90-47e0-949a-a1498ed7f82e">SetFormat</a>
</td>
<td align="left" width="63%">
Sets the image format of the frames being extracted.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

