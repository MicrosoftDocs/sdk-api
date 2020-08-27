---
UID: NN:mergemod.IMsmConfigurableItem
title: IMsmConfigurableItem (mergemod.h)
description: The IMsmConfigurableItem interface manages a single row from the ModuleConfiguration table. This is a single configurable &quot;attribute&quot; from the module. The interface consists of read-only properties, one for each column in the ModuleConfiguration table.
helpviewer_keywords: ["IMsmConfigurableItem","IMsmConfigurableItem interface","IMsmConfigurableItem interface","described","mergemod/IMsmConfigurableItem","setup.imsmconfigurableitem_interface"]
old-location: setup\imsmconfigurableitem_interface.htm
tech.root: setup
ms.assetid: d10bfd31-22a8-4100-ac0b-dd0795622808
ms.date: 12/05/2018
ms.keywords: IMsmConfigurableItem, IMsmConfigurableItem interface, IMsmConfigurableItem interface,described, mergemod/IMsmConfigurableItem, setup.imsmconfigurableitem_interface
f1_keywords:
- mergemod/IMsmConfigurableItem
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMsmConfigurableItem interface


## -description


The <b>IMsmConfigurableItem</b> interface manages a single row from the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/moduleconfiguration-table">ModuleConfiguration table</a>. This is a single configurable "attribute" from the module. The interface consists of read-only properties, one for each column in the ModuleConfiguration table. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmConfigurableItem</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMsmConfigurableItem</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfigurableitem-get_attributes">get_Attributes</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/configurableitem-attributes">Attributes</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfigurableitem-get_context">get_Context</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/configurableitem-context">Context</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfigurableitem-get_defaultvalue">get_DefaultValue</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/configurableitem-defaultvalue">DefaultValue</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfigurableitem-get_description">get_Description</a>
</td>
<td align="left" width="63%">
Retrieves 
the <a href="https://docs.microsoft.com/windows/desktop/Msi/configurableitem-description">Description</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfigurableitem-get_displayname">get_DisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/configurableitem-displayname">DisplayName</a> property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfigurableitem-get_format">get_Format</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/configurableitem-format">Format</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfigurableitem-get_helpkeyword">get_HelpKeyword</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/configurableitem-helpkeyword">HelpKeyword</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfigurableitem-get_helplocation">get_HelpLocation</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/configurableitem-helplocation">HelpLocation</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfigurableitem-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/configurableitem-name">Name</a> property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmconfigurableitem-get_type">get_Type</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/configurableitem-type">Type</a> property.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>
 

 

