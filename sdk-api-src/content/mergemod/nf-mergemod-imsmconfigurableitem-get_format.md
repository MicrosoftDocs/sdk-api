---
UID: NF:mergemod.IMsmConfigurableItem.get_Format
title: IMsmConfigurableItem::get_Format
author: windows-sdk-content
description: The Format property of the ConfigurableItem object returns the value from the Format column of the ModuleConfiguration table.
old-location: setup\configurableitem_format.htm
old-project: msi
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ConfigurableItem object,Format property, ConfigurableItem.Format, Format property, Format property,ConfigurableItem object, IMsmConfigurableItem.get_Format, IMsmConfigurableItem::get_Format, _msi_format_property, get_Format, setup.configurableitem_format
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 2.0 or later
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
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - ConfigurableItem.Format
 - IMsmConfigurableItem.get_Format
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmConfigurableItem::get_Format


## -description


The 
<b>Format</b> property of the 
<a href="https://msdn.microsoft.com/bbd0d9bc-a463-4cd8-93ee-963dcee8efa6">ConfigurableItem</a> object returns the value from the Format column of the 
<a href="https://msdn.microsoft.com/3b77cc23-c104-4adc-868c-3aa2b5794bc7">ModuleConfiguration table</a>.

This property is read-only.


## -parameters


## -remarks



This property can only have the following values.

<table>
<tr>
<th>Constant</th>
<th>Value</th>
</tr>
<tr>
<td><b>msmConfigurableItemText</b></td>
<td>0</td>
</tr>
<tr>
<td><b>msmConfigurableItemKey</b></td>
<td>1</td>
</tr>
<tr>
<td><b>msmConfigurableItemInteger</b></td>
<td>2</td>
</tr>
<tr>
<td><b>msmConfigurableItemBitfield</b></td>
<td>3</td>
</tr>
</table>
 

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/85db7d8b-e3f2-4a7a-840f-2d690aa82917">get_Format</a> function.



