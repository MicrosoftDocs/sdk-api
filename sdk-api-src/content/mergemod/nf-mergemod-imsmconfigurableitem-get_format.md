---
UID: NF:mergemod.IMsmConfigurableItem.get_Format
title: IMsmConfigurableItem::get_Format (mergemod.h)
description: The get_Format method retrieves the Format property of the ConfigurableItem object.
helpviewer_keywords: ["IMsmConfigurableItem interface","get_Format method","IMsmConfigurableItem.get_Format","IMsmConfigurableItem::get_Format","_msi_get_format_function","get_Format","get_Format method","get_Format method","IMsmConfigurableItem interface","mergemod/IMsmConfigurableItem::get_Format","setup.imsmconfigurableitem_get_format"]
old-location: setup\imsmconfigurableitem_get_format.htm
tech.root: setup
ms.assetid: 85db7d8b-e3f2-4a7a-840f-2d690aa82917
ms.date: 12/05/2018
ms.keywords: IMsmConfigurableItem interface,get_Format method, IMsmConfigurableItem.get_Format, IMsmConfigurableItem::get_Format, _msi_get_format_function, get_Format, get_Format method, get_Format method,IMsmConfigurableItem interface, mergemod/IMsmConfigurableItem::get_Format, setup.imsmconfigurableitem_get_format
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
 - IMsmConfigurableItem::get_Format
 - mergemod/IMsmConfigurableItem::get_Format
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
 - IMsmConfigurableItem.get_Format
---

# IMsmConfigurableItem::get_Format


## -description

The 
<b>get_Format</b> method retrieves the 
<a href="/windows/desktop/Msi/configurableitem-format">Format</a> property of the 
<a href="/windows/desktop/Msi/configurableitem-object">ConfigurableItem</a> object.

## -parameters

### -param Format [out]

A pointer to a location in memory with the format of a configurable item listed in the Format column of the 
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