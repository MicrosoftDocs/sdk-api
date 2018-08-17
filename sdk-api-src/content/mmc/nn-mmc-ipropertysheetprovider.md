---
UID: NN:mmc.IPropertySheetProvider
title: IPropertySheetProvider
author: windows-sdk-content
description: The IPropertySheetProvider interface implements Windows property sheets as COM objects.
old-location: mmc\ipropertysheetprovider.htm
old-project: mmc
ms.assetid: c63d5d5f-a334-4367-8a1e-252b4eb5b50d
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IPropertySheetProvider, IPropertySheetProvider interface [MMC], IPropertySheetProvider interface [MMC],described, _slate_ipropertysheetprovider, mmc.ipropertysheetprovider, mmc/IPropertySheetProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmc.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IPropertySheetProvider
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IPropertySheetProvider interface


## -description


The 
<b>IPropertySheetProvider</b> interface implements Windows property sheets as COM objects. A property sheet object contains the code required to handle modeless operation and determining which other snap-ins are extending the node type. The size of the property sheet is set by the primary snap-in and extensions are forced to accept that size.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertySheetProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertySheetProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertySheetProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a2ce7a6-65d6-4e39-b8b8-8d9b59b32d11">AddExtensionPages</a>
</td>
<td align="left" width="63%">
Collects pages from one or more extension snap-ins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f555dfd0-8af3-422f-a339-ab79daa89b45">AddPrimaryPages</a>
</td>
<td align="left" width="63%">
Collects property pages from the primary snap-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d53083a-d578-4a88-bd3f-d43c88d697e5">CreatePropertySheet</a>
</td>
<td align="left" width="63%">
Creates a property sheet frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14f3a2b7-9e14-4068-a85a-20c41d7e4a4d">FindPropertySheet</a>
</td>
<td align="left" width="63%">
Determines whether a property sheet exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08e1e3d9-9c9e-49c8-9d55-31c9519c5b0c">Show</a>
</td>
<td align="left" width="63%">
Displays a specific property sheet frame.

</td>
</tr>
</table> 

