---
UID: NN:callobj.ICallFrameWalker
title: ICallFrameWalker
author: windows-sdk-content
description: Walks a stack frame looking for interesting values.
old-location: com\icallframewalker.htm
tech.root: com
ms.assetid: 1eeb00a3-d3c5-46f0-95a8-f694f802894b
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: ICallFrameWalker, ICallFrameWalker interface [COM], ICallFrameWalker interface [COM],described, _com_icallframewalker, callobj/ICallFrameWalker, com.icallframewalker
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
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
 - Callobj.h
api_name:
 - ICallFrameWalker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICallFrameWalker interface


## -description


Walks a stack frame looking for interesting values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallFrameWalker</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICallFrameWalker</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICallFrameWalker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms693762(v=VS.85).aspx">OnWalkInterface</a>
</td>
<td align="left" width="63%">
Walks through a call frame to look for the specified interface in the call frame.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms683962(v=VS.85).aspx">ICallFrame::WalkFrame</a>
 

 

