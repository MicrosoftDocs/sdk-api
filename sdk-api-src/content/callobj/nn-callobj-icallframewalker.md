---
UID: NN:callobj.ICallFrameWalker
title: ICallFrameWalker (callobj.h)
author: windows-sdk-content
description: Walks a stack frame looking for interesting values.
old-location: com\icallframewalker.htm
tech.root: com
ms.assetid: 1eeb00a3-d3c5-46f0-95a8-f694f802894b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICallFrameWalker, ICallFrameWalker interface [COM], ICallFrameWalker interface [COM],described, _com_icallframewalker, callobj/ICallFrameWalker, com.icallframewalker
ms.topic: interface
f1_keywords: 
 - "callobj/ICallFrameWalker"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICallFrameWalker interface


## -description


Walks a stack frame looking for interesting values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallFrameWalker</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICallFrameWalker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframewalker-onwalkinterface">OnWalkInterface</a>
</td>
<td align="left" width="63%">
Walks through a call frame to look for the specified interface in the call frame.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-walkframe">ICallFrame::WalkFrame</a>
 

 

