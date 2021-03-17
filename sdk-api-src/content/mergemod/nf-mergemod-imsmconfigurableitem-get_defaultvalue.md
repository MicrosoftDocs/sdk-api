---
UID: NF:mergemod.IMsmConfigurableItem.get_DefaultValue
title: IMsmConfigurableItem::get_DefaultValue (mergemod.h)
description: The get_DefaultValue method retrieves the DefaultValue property of the ConfigurableItem object.
helpviewer_keywords: ["IMsmConfigurableItem interface","get_DefaultValue method","IMsmConfigurableItem.get_DefaultValue","IMsmConfigurableItem::get_DefaultValue","_msi_get_defaultvalue_function","get_DefaultValue","get_DefaultValue method","get_DefaultValue method","IMsmConfigurableItem interface","mergemod/IMsmConfigurableItem::get_DefaultValue","setup.imsmconfigurableitem_get_defaultvalue"]
old-location: setup\imsmconfigurableitem_get_defaultvalue.htm
tech.root: setup
ms.assetid: b62e5a8c-4b1f-4d9e-9df6-6438e715e16a
ms.date: 12/05/2018
ms.keywords: IMsmConfigurableItem interface,get_DefaultValue method, IMsmConfigurableItem.get_DefaultValue, IMsmConfigurableItem::get_DefaultValue, _msi_get_defaultvalue_function, get_DefaultValue, get_DefaultValue method, get_DefaultValue method,IMsmConfigurableItem interface, mergemod/IMsmConfigurableItem::get_DefaultValue, setup.imsmconfigurableitem_get_defaultvalue
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
 - IMsmConfigurableItem::get_DefaultValue
 - mergemod/IMsmConfigurableItem::get_DefaultValue
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
 - IMsmConfigurableItem.get_DefaultValue
---

# IMsmConfigurableItem::get_DefaultValue


## -description

The 
<b>get_DefaultValue</b> method retrieves the 
<a href="/windows/desktop/Msi/configurableitem-defaultvalue">DefaultValue</a> property of the 
<a href="/windows/desktop/Msi/configurableitem-object">ConfigurableItem</a> object.

## -parameters

### -param DefaultValue [out]

A pointer to a location in memory with the default value of a configurable item listed in the DefaultValue column of the 
<a href="/windows/desktop/Msi/moduleconfiguration-table">ModuleConfiguration table</a>. The client must free the <b>BSTR</b> when it is no longer required.

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
</table>

## -see-also

<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmconfigurableitem">IMsmConfigurableItem</a>



<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>