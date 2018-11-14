---
UID: NN:xamlom.IVisualTreeService
title: IVisualTreeService
author: windows-sdk-content
description: Provides methods to manage a XAML visual tree.
old-location: xaml_diagnostics\ivisualtreeservice.htm
tech.root: xaml_diagnostics
ms.assetid: 5C0896E4-E37E-49DF-B303-1814BCA6F5B3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVisualTreeService, IVisualTreeService interface, IVisualTreeService interface,described, xaml_diagnostics.ivisualtreeservice, xamlom/IVisualTreeService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xamlom.h
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
 - xamlom.h
api_name:
 - IVisualTreeService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVisualTreeService interface


## -description


Provides methods to manage a XAML visual tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVisualTreeService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVisualTreeService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVisualTreeService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0F3BFACA-0B4C-4CC5-A48B-BD3921728612">AddChild</a>
</td>
<td align="left" width="63%">
Adds a child element to the collection at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83971154-4E40-474C-91AD-2436B1D02CB8">AdviseVisualTreeChange</a>
</td>
<td align="left" width="63%">
Starts listening for changes to the visual tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E32B07F5-BB62-435A-A869-36A0E93915D9">ClearChildren</a>
</td>
<td align="left" width="63%">
Clears all child elements from the parent collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BB875AD0-271D-4913-9811-5A5102B3E331">ClearProperty</a>
</td>
<td align="left" width="63%">
Clears the specified property on a XAML element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/214BE795-5883-4761-9040-2C7A679F5258">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an instance of any XAML runtime, enum, or primitive type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BB6D0885-27BD-4DF6-A48A-570345F1EE14">GetCollectionCount</a>
</td>
<td align="left" width="63%">
Gets the count of a collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01A2694F-E9CF-4DD2-95EA-6CD5C72C65A8">GetCollectionElements</a>
</td>
<td align="left" width="63%">
Gets the elements in a collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95D6F754-C1D0-4B8E-8E31-999CAE0EDF02">GetEnums</a>
</td>
<td align="left" width="63%">
Gets an array of all the enums defined in the XAML runtime and the total
    count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3D997B09-7B20-47BC-B19C-98945CA41D17">GetPropertyValuesChain</a>
</td>
<td align="left" width="63%">
Gets an array of all the
    properties set on the element passed in, and an array of all the styles involved in setting the effective values of the properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6D53C961-7E85-4275-8D65-454684606290">RemoveChild</a>
</td>
<td align="left" width="63%">
Removes the child element from the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A9C6C67F-7767-454C-BA05-86C6B1E5D712">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a property value on a XAML element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E77CBED8-F214-48AC-903E-F01B6EECA2ED">UnadviseVisualTreeChange</a>
</td>
<td align="left" width="63%">
Stops listening for changes to the visual tree.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

