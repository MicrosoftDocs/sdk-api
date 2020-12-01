---
UID: NF:mergemod.IMsmMerge2.get_ConfigurableItems
title: IMsmMerge2::get_ConfigurableItems (mergemod.h)
description: The get_ConfigurableItems method retrieves the ConfigurableItems property of the Merge object.
helpviewer_keywords: ["IMsmMerge2 interface","get_ConfigurableItems method","IMsmMerge2.get_ConfigurableItems","IMsmMerge2::get_ConfigurableItems","_msi_get_configurableitems_function","get_ConfigurableItems","get_ConfigurableItems method","get_ConfigurableItems method","IMsmMerge2 interface","mergemod/IMsmMerge2::get_ConfigurableItems","setup.imsmmerge2_get_configurableitems"]
old-location: setup\imsmmerge2_get_configurableitems.htm
tech.root: setup
ms.assetid: c8b34ff7-6b0b-4cd9-bcb2-9d0da6b14254
ms.date: 12/05/2018
ms.keywords: IMsmMerge2 interface,get_ConfigurableItems method, IMsmMerge2.get_ConfigurableItems, IMsmMerge2::get_ConfigurableItems, _msi_get_configurableitems_function, get_ConfigurableItems, get_ConfigurableItems method, get_ConfigurableItems method,IMsmMerge2 interface, mergemod/IMsmMerge2::get_ConfigurableItems, setup.imsmmerge2_get_configurableitems
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
 - IMsmMerge2::get_ConfigurableItems
 - mergemod/IMsmMerge2::get_ConfigurableItems
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
 - IMsmMerge2.get_ConfigurableItems
---

# IMsmMerge2::get_ConfigurableItems


## -description

The 
<b>get_ConfigurableItems</b> method retrieves the 
<a href="/windows/desktop/Msi/merge-configurableitems">ConfigurableItems</a> property of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object.

## -parameters

### -param ConfigurableItems [out]

Pointer to a memory location containing another pointer to an <b>IMsmConfigurableItems</b> interface.

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
The <i>ConfigurableItems</i> pointer is <b>NULL</b>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system ran out of memory.

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

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>