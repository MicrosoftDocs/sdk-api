---
UID: NF:mergemod.IMsmConfigurableItem.get_Attributes
title: IMsmConfigurableItem::get_Attributes (mergemod.h)
description: The get_Attributes method retrieves the Attributes property of the ConfigurableItem object.
helpviewer_keywords: ["IMsmConfigurableItem interface","get_Attributes method","IMsmConfigurableItem.get_Attributes","IMsmConfigurableItem::get_Attributes","_msi_get_attributes_function","get_Attributes","get_Attributes method","get_Attributes method","IMsmConfigurableItem interface","mergemod/IMsmConfigurableItem::get_Attributes","setup.imsmconfigurableitem_get_attributes"]
old-location: setup\imsmconfigurableitem_get_attributes.htm
tech.root: setup
ms.assetid: 347451e9-0623-4d31-a9f5-7cb95f234717
ms.date: 12/05/2018
ms.keywords: IMsmConfigurableItem interface,get_Attributes method, IMsmConfigurableItem.get_Attributes, IMsmConfigurableItem::get_Attributes, _msi_get_attributes_function, get_Attributes, get_Attributes method, get_Attributes method,IMsmConfigurableItem interface, mergemod/IMsmConfigurableItem::get_Attributes, setup.imsmconfigurableitem_get_attributes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmConfigurableItem::get_Attributes
 - mergemod/IMsmConfigurableItem::get_Attributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmConfigurableItem.get_Attributes
---

# IMsmConfigurableItem::get_Attributes


## -description

The 
<b>get_Attributes</b> method retrieves the 
<a href="/windows/desktop/Msi/configurableitem-attributes">Attributes</a> property of the 
<a href="/windows/desktop/Msi/configurableitem-object">ConfigurableItem</a> object.

## -parameters

### -param Attributes [out]

A pointer to a location in memory with the format of a configurable item listed in the Attributes column of the 
<a href="/windows/desktop/Msi/moduleconfiguration-table">ModuleConfiguration table</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No module is open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
The function failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
The function failed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmconfigurableitem">IMsmConfigurableItem</a>



<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>