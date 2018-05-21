---
UID: NN:strmif.IGraphVersion
title: IGraphVersion
author: windows-driver-content
description: The IGraphVersion interface is implemented on the Filter Graph Manager to provide a way for plug-in distributors and applications to know when the graph has changed.
old-location: dshow\igraphversion.htm
old-project: DirectShow
ms.assetid: abca59f2-2134-4938-9933-bacaed771d0d
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IGraphVersion, IGraphVersion interface [DirectShow], IGraphVersion interface [DirectShow],described, IGraphVersionInterface, dshow.igraphversion, strmif/IGraphVersion
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IGraphVersion
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGraphVersion interface


## -description



The <code>IGraphVersion</code> interface is implemented on the Filter Graph Manager to provide a way for plug-in distributors and applications to know when the graph has changed. If the graph has changed, and the application or plug-in distributor has an interface on a particular filter or pin, it should requery the graph to see if its pointers are still valid, or if there are new ones it should use.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGraphVersion</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGraphVersion</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGraphVersion</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/297e19fd-91b5-4756-9b33-6b301c74e470">QueryVersion</a>
</td>
<td align="left" width="63%">
Retrieves the current graph version number.

</td>
</tr>
</table> 

