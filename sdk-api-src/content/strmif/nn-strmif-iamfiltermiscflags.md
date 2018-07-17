---
UID: NN:strmif.IAMFilterMiscFlags
title: IAMFilterMiscFlags
author: windows-sdk-content
description: The IAMFilterMiscFlags interface queries whether a filter is a source filter or a renderer.
old-location: dshow\iamfiltermiscflags.htm
old-project: DirectShow
ms.assetid: f9f3eaf9-4afa-412f-aa8f-b75e787cfecb
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IAMFilterMiscFlags, IAMFilterMiscFlags interface [DirectShow], IAMFilterMiscFlags interface [DirectShow],described, IAMFilterMiscFlagsInterface, dshow.iamfiltermiscflags, strmif/IAMFilterMiscFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMFilterMiscFlags
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMFilterMiscFlags interface


## -description



The <code>IAMFilterMiscFlags</code> interface queries whether a filter is a source filter or a renderer. Source and renderer filters should implement this interface.

Applications do not use this interface. The Filter Graph Manager uses this interface to determine how many <a href="https://msdn.microsoft.com/46037d53-085d-4fd0-91a0-408702cbfce5">EC_COMPLETE</a> events it will receive when playback completes.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMFilterMiscFlags</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMFilterMiscFlags</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMFilterMiscFlags</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03728d28-a3e5-4ac5-b637-1daa173e5e88">GetMiscFlags</a>
</td>
<td align="left" width="63%">
Returns the filter's type, either source or renderer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

