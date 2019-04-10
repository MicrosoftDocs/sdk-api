---
UID: NN:mergemod.IMsmConfigurableItem
title: IMsmConfigurableItem (mergemod.h)
author: windows-sdk-content
description: The IMsmConfigurableItem interface manages a single row from the ModuleConfiguration table. This is a single configurable &#0034;attribute&#0034; from the module. The interface consists of read-only properties, one for each column in the ModuleConfiguration table.
old-location: setup\imsmconfigurableitem_interface.htm
tech.root: Msi
ms.assetid: d10bfd31-22a8-4100-ac0b-dd0795622808
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMsmConfigurableItem, IMsmConfigurableItem interface, IMsmConfigurableItem interface,described, mergemod/IMsmConfigurableItem, setup.imsmconfigurableitem_interface
ms.topic: interface
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmConfigurableItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmConfigurableItem interface


## -description


The <b>IMsmConfigurableItem</b> interface manages a single row from the 
<a href="https://msdn.microsoft.com/3b77cc23-c104-4adc-868c-3aa2b5794bc7">ModuleConfiguration table</a>. This is a single configurable "attribute" from the module. The interface consists of read-only properties, one for each column in the ModuleConfiguration table. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmConfigurableItem</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMsmConfigurableItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMsmConfigurableItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/347451e9-0623-4d31-a9f5-7cb95f234717">get_Attributes</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/fb7336b7-28af-48c8-80b2-80c03948660a">Attributes</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90aa0ee2-a7eb-464c-8a8f-ed4bdf46990e">get_Context</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/27b94142-81cb-4ea7-aa73-c359cb50ce71">Context</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b62e5a8c-4b1f-4d9e-9df6-6438e715e16a">get_DefaultValue</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/2d99ee59-5dea-41ca-bd24-359195a37864">DefaultValue</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aafc79a0-51cb-4147-b72c-b5218835dc03">get_Description</a>
</td>
<td align="left" width="63%">
Retrieves 
the <a href="https://msdn.microsoft.com/a43e3392-0539-4904-a0d9-827b69e1ce07">Description</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f947e570-251d-4638-b8b8-aaa6f08bde46">get_DisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/f2025bab-73b0-46d2-a276-0ad17fdd9783">DisplayName</a> property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85db7d8b-e3f2-4a7a-840f-2d690aa82917">get_Format</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/e75ed650-7309-4e24-9c35-82ebf27d011b">Format</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75dc8672-f910-448a-906b-aba921463e78">get_HelpKeyword</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/470db520-3a9a-47bf-90ff-a284bafa1020">HelpKeyword</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a66f2934-048e-4df2-a004-287faf42445d">get_HelpLocation</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/fe011188-c831-4fbd-b2dd-1ad4c08451ed">HelpLocation</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/310fcf76-457b-43d0-b33b-181b32480042">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/c28f508f-0788-4b60-a383-65c508ceef5f">Name</a> property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18745546-1aa7-4f52-9eba-adfedb46753a">get_Type</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/af2cb859-2e9d-4bca-867b-cdc61d9758cd">Type</a> property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

