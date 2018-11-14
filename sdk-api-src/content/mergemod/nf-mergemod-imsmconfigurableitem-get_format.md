---
UID: NF:mergemod.IMsmConfigurableItem.get_Format
title: IMsmConfigurableItem::get_Format
author: windows-sdk-content
description: The get_Format method retrieves the Format property of the ConfigurableItem object.
old-location: setup\imsmconfigurableitem_get_format.htm
tech.root: msi
ms.assetid: 85db7d8b-e3f2-4a7a-840f-2d690aa82917
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMsmConfigurableItem interface,get_Format method, IMsmConfigurableItem.get_Format, IMsmConfigurableItem::get_Format, _msi_get_format_function, get_Format, get_Format method, get_Format method,IMsmConfigurableItem interface, mergemod/IMsmConfigurableItem::get_Format, setup.imsmconfigurableitem_get_format
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMsmConfigurableItem.get_Format
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mergemod.h
: 
- IMsmConfigurableItem.get_Format
: 
---

# IMsmConfigurableItem::get_Format


## -description


The 
<b>get_Format</b> method retrieves the 
<a href="https://msdn.microsoft.com/e75ed650-7309-4e24-9c35-82ebf27d011b">Format</a> property of the 
<a href="https://msdn.microsoft.com/bbd0d9bc-a463-4cd8-93ee-963dcee8efa6">ConfigurableItem</a> object.


## -parameters




### -param Format [out]

A pointer to a location in memory with the format of a configurable item listed in the Format column of the 
<a href="https://msdn.microsoft.com/3b77cc23-c104-4adc-868c-3aa2b5794bc7">ModuleConfiguration table</a>.


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




<a href="https://msdn.microsoft.com/d10bfd31-22a8-4100-ac0b-dd0795622808">IMsmConfigurableItem</a>



<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

