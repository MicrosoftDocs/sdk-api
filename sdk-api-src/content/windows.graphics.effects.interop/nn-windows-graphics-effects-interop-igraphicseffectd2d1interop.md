---
UID: NN:windows.graphics.effects.interop.IGraphicsEffectD2D1Interop
title: IGraphicsEffectD2D1Interop (windows.graphics.effects.interop.h)
author: windows-sdk-content
description: Native interoperation interface that provides a counterpart to IGraphicsEffect and allows for metadata queries. This interface is available in C++ only.
old-location: w_graph_fx\igraphicseffectd2d1interop.htm
tech.root: w_graph_fx
ms.assetid: 0D576593-088B-403A-82AD-B7A89777766A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGraphicsEffectD2D1Interop, IGraphicsEffectD2D1Interop interface, IGraphicsEffectD2D1Interop interface,described, w_graph_fx.igraphicseffectd2d1interop, windows/IGraphicsEffectD2D1Interop
ms.topic: interface
req.header: windows.graphics.effects.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - windows.graphics.effects.interop.h
api_name:
 - IGraphicsEffectD2D1Interop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGraphicsEffectD2D1Interop interface


## -description


Native interoperation interface that provides a counterpart to <a href="https://msdn.microsoft.com/c88277a4-6697-4341-9b8b-dffa470fd37e">IGraphicsEffect</a> and allows for metadata queries. 

        This interface is available in C++ only.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGraphicsEffectD2D1Interop</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGraphicsEffectD2D1Interop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGraphicsEffectD2D1Interop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75870414-23B4-4157-94DC-F03E0A978EF3">GetEffectId</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72185CB5-6D8A-4F9F-B913-C9216CECEC90">GetNamedPropertyMapping</a>
</td>
<td align="left" width="63%">
Retrieves the mapping for an effect property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/415C12FA-C779-4F00-A83F-AB5D4EC0B8C2">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the effect property at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B1A89551-72B3-4C30-B75F-5159DD774E04">GetPropertyCount</a>
</td>
<td align="left" width="63%">
Retrieve the property count for the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C4A212ED-EE68-40D7-B6E0-977F748942BB">GetSource</a>
</td>
<td align="left" width="63%">
Retrieves the effect source at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C2287E81-4CCC-471B-833C-84B37F245084">GetSourceCount</a>
</td>
<td align="left" width="63%">
Retrieves the source count for the effect.

</td>
</tr>
</table> 

