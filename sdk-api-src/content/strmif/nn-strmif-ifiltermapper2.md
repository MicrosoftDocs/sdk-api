---
UID: NN:strmif.IFilterMapper2
title: IFilterMapper2
author: windows-sdk-content
description: Registers and unregisters filters, and locates filters in the registry.
old-location: dshow\ifiltermapper2.htm
old-project: DirectShow
ms.assetid: 6a3db838-cee3-4a9f-a924-fb55931acc83
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IFilterMapper2, IFilterMapper2 interface [DirectShow], IFilterMapper2 interface [DirectShow],described, IFilterMapper2Interface, dshow.ifiltermapper2, strmif/IFilterMapper2
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
-	IFilterMapper2
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterMapper2 interface


## -description



Registers and unregisters filters, and locates filters in the registry. The <a href="https://msdn.microsoft.com/cb8f25b3-a0f0-48fa-843f-88a5a5d17019">Filter Mapper</a> helper object implements this interface.

Filters use this interface to register and unregister themselves. When the filter graph manager builds a filter graph, it uses this interface to look up filters and determine their characteristics. Applications can also use this interface to look up filters. For more information, see <a href="https://msdn.microsoft.com/3f774350-4508-437f-98d1-cca91220f339">Using the Filter Mapper</a> and <a href="https://msdn.microsoft.com/2b6304c0-4b67-4723-94a0-7b1fff534f91">How to Register DirectShow Filters</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterMapper2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFilterMapper2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterMapper2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37dc50a0-530c-4b31-b766-9e161b04c6d5">CreateCategory</a>
</td>
<td align="left" width="63%">
Adds a new filter category to the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f121b4c3-fce1-4be3-ace4-5084242130f6">EnumMatchingFilters</a>
</td>
<td align="left" width="63%">
Enumerates registered filters that meet specified requirements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/773e527e-2174-4f74-a822-549cfe2927a3">RegisterFilter</a>
</td>
<td align="left" width="63%">
Adds filter information to the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfba764d-ec94-49a2-9aaf-2b107b742f83">UnregisterFilter</a>
</td>
<td align="left" width="63%">
Removes filter information from the registry.

</td>
</tr>
</table> 

