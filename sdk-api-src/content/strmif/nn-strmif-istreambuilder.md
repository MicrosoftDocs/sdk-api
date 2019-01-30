---
UID: NN:strmif.IStreamBuilder
title: IStreamBuilder
author: windows-sdk-content
description: The IStreamBuilder interface enables an output pin to notify the filter graph manager that the pin itself will build the downstream section of the filter graph.
old-location: dshow\istreambuilder.htm
tech.root: DirectShow
ms.assetid: 233821e9-9916-4047-a554-4ff43769819f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStreamBuilder, IStreamBuilder interface [DirectShow], IStreamBuilder interface [DirectShow],described, IStreamBuilderInterface, dshow.istreambuilder, strmif/IStreamBuilder
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IStreamBuilder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBuilder interface


## -description



The <code>IStreamBuilder</code> interface enables an output pin to notify the filter graph manager that the pin itself will build the downstream section of the filter graph. Output pins with special connection needs can implement this interface to override the default pin connection process used by the filter graph manager.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBuilder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8f895a7-7f71-4c0d-af9d-e2b0ed433172">Backout</a>
</td>
<td align="left" width="63%">
Undoes steps taken in <b>Render</b>. This includes disconnecting and removing any filters that were added inside <b>Render</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bba9d1a-03a8-4572-a08c-2e12071df73b">Render</a>
</td>
<td align="left" width="63%">
Completes rendering of the stream originating with this pin. This can involve adding filters to the filter graph and connecting them.

</td>
</tr>
</table> 

