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
ms.custom: 19H1
---

# IGraphicsEffectD2D1Interop interface


## -description


Native interoperation interface that provides a counterpart to <a href="https://msdn.microsoft.com/c88277a4-6697-4341-9b8b-dffa470fd37e">IGraphicsEffect</a> and allows for metadata queries. 

        This interface is available in C++ only.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGraphicsEffectD2D1Interop</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGraphicsEffectD2D1Interop</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/windows.graphics.effects.interop/nf-windows-graphics-effects-interop-igraphicseffectd2d1interop-geteffectid">GetEffectId</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.graphics.effects.interop/nf-windows-graphics-effects-interop-igraphicseffectd2d1interop-getnamedpropertymapping">GetNamedPropertyMapping</a>
</td>
<td align="left" width="63%">
Retrieves the mapping for an effect property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.graphics.effects.interop/nf-windows-graphics-effects-interop-igraphicseffectd2d1interop-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the effect property at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.graphics.effects.interop/nf-windows-graphics-effects-interop-igraphicseffectd2d1interop-getpropertycount">GetPropertyCount</a>
</td>
<td align="left" width="63%">
Retrieve the property count for the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.graphics.effects.interop/nf-windows-graphics-effects-interop-igraphicseffectd2d1interop-getsource">GetSource</a>
</td>
<td align="left" width="63%">
Retrieves the effect source at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.graphics.effects.interop/nf-windows-graphics-effects-interop-igraphicseffectd2d1interop-getsourcecount">GetSourceCount</a>
</td>
<td align="left" width="63%">
Retrieves the source count for the effect.

</td>
</tr>
</table> 

