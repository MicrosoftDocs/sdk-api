---
UID: NF:mergemod.IMsmConfigurableItem.get_HelpLocation
title: IMsmConfigurableItem::get_HelpLocation (mergemod.h)
description: The get_HelpLocation method retrieves the HelpLocation property of the ConfigurableItem object.
helpviewer_keywords: ["IMsmConfigurableItem interface","get_HelpLocation method","IMsmConfigurableItem.get_HelpLocation","IMsmConfigurableItem::get_HelpLocation","_msi_get_helplocation_function","get_HelpLocation","get_HelpLocation method","get_HelpLocation method","IMsmConfigurableItem interface","mergemod/IMsmConfigurableItem::get_HelpLocation","setup.imsmconfigurableitem_get_helplocation"]
old-location: setup\imsmconfigurableitem_get_helplocation.htm
tech.root: setup
ms.assetid: a66f2934-048e-4df2-a004-287faf42445d
ms.date: 12/05/2018
ms.keywords: IMsmConfigurableItem interface,get_HelpLocation method, IMsmConfigurableItem.get_HelpLocation, IMsmConfigurableItem::get_HelpLocation, _msi_get_helplocation_function, get_HelpLocation, get_HelpLocation method, get_HelpLocation method,IMsmConfigurableItem interface, mergemod/IMsmConfigurableItem::get_HelpLocation, setup.imsmconfigurableitem_get_helplocation
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
 - IMsmConfigurableItem::get_HelpLocation
 - mergemod/IMsmConfigurableItem::get_HelpLocation
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
 - IMsmConfigurableItem.get_HelpLocation
---

# IMsmConfigurableItem::get_HelpLocation


## -description

The 
<b>get_HelpLocation</b> method retrieves the 
<a href="/windows/desktop/Msi/configurableitem-helplocation">HelpLocation</a> property of the 
<a href="/windows/desktop/Msi/configurableitem-object">ConfigurableItem</a> object.

## -parameters

### -param HelpLocation [out]

A pointer to a location in memory with the help location of a configurable item listed in the HelpLocation column of the 
<a href="/windows/desktop/Msi/moduleconfiguration-table">ModuleConfiguration table</a>. The client must free the <b>BSTR</b> when it is no longer needed.

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