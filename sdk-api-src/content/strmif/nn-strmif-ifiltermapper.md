---
UID: NN:strmif.IFilterMapper
title: IFilterMapper
author: windows-sdk-content
description: Note  This interface has been deprecated.
old-location: dshow\ifiltermapper.htm
old-project: DirectShow
ms.assetid: e2f32235-e331-4c3c-925a-7cfa531e9ab3
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IFilterMapper, IFilterMapper interface [DirectShow], IFilterMapper interface [DirectShow],described, IFilterMapperInterface, dshow.ifiltermapper, strmif/IFilterMapper
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IFilterMapper
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterMapper interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use the <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a> interface.</div>
<div> </div>
This interface provides methods for registering and unregistering filters, and for looking up filters based on their characteristics.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterMapper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFilterMapper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterMapper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/602a7568-f5f8-4705-a2bc-6b9408bbbe54">EnumMatchingFilters</a>
</td>
<td align="left" width="63%">
Finds all filters matching specific requirements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e21da510-f4e6-417e-978d-bb53bf78cf94">RegisterFilter</a>
</td>
<td align="left" width="63%">
Records the details of a filter in the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce42047c-0b74-4ad4-b5a1-ea66fc6bffc3">RegisterFilterInstance</a>
</td>
<td align="left" width="63%">
Registers an identifiable instance of a filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fd0072f-e63f-41e2-b8f1-821c3c0e0f4e">RegisterPin</a>
</td>
<td align="left" width="63%">
Records the details of a pin in the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f92745b-2b97-4cc6-9755-a580827b5bba">RegisterPinType</a>
</td>
<td align="left" width="63%">
Adds a type for the pin to the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b5941d4-d0e7-4f4a-b273-e0fa4a1e1c2e">UnregisterFilter</a>
</td>
<td align="left" width="63%">
Deletes a filter from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfeb0129-f67c-4318-8206-aa08e3b5b370">UnregisterFilterInstance</a>
</td>
<td align="left" width="63%">
Deletes an identifiable instance of a filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8964890-53d7-4731-91b2-156e61809774">UnregisterPin</a>
</td>
<td align="left" width="63%">
Deletes a pin from the registry.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>
 

 

