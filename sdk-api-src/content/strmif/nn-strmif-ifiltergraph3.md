---
UID: NN:strmif.IFilterGraph3
title: IFilterGraph3
author: windows-driver-content
description: The IFilterGraph3 interface extends the IFilterGraph2 interface, which contains methods for building filter graphs.The Filter Graph Manager implements this interface.
old-location: dshow\ifiltergraph3.htm
old-project: DirectShow
ms.assetid: 1d5f8eda-2b09-4627-8ae9-f43f38c3c26a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IFilterGraph3, IFilterGraph3 interface [DirectShow], IFilterGraph3 interface [DirectShow],described, IFilterGraph3Interface, dshow.ifiltergraph3, strmif/IFilterGraph3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IFilterGraph3
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterGraph3 interface


## -description



The <code>IFilterGraph3</code> interface extends the <a href="https://msdn.microsoft.com/1a1ef4fe-a054-4ba7-99c7-1f209472c5a6">IFilterGraph2</a> interface, which contains methods for building filter graphs.

The Filter Graph Manager implements this interface. Applications can use it when building graphs, to take advantage of the additional methods it provides.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterGraph3</b> interface inherits from <b>IFilterGraph2</b>. <b>IFilterGraph3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterGraph3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/153a0584-d613-499d-8dbb-c4207c7f60b3">SetSyncSourceEx</a>
</td>
<td align="left" width="63%">
Sets a primary and secondary reference clock for the filter graph.

</td>
</tr>
</table> 

