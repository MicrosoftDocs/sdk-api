---
UID: NF:mergemod.IMsmConfigurableItem.get_Context
title: IMsmConfigurableItem::get_Context method
author: windows-driver-content
description: The get_Context method retrieves the Context property of the ConfigurableItem object.
old-location: setup\imsmconfigurableitem_get_context.htm
old-project: Msi
ms.assetid: 90aa0ee2-a7eb-464c-8a8f-ed4bdf46990e
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMsmConfigurableItem, IMsmConfigurableItem interface, get_Context method, IMsmConfigurableItem::get_Context, _msi_get_context_function, get_Context method, get_Context method, IMsmConfigurableItem interface, get_Context,IMsmConfigurableItem.get_Context, mergemod/IMsmConfigurableItem::get_Context, setup.imsmconfigurableitem_get_context
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
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mergemod.dll
api_name:
-	IMsmConfigurableItem.get_Context
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmConfigurableItem::get_Context method


## -description


The 
<b>get_Context</b> method retrieves the 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">Context</a> property of the 
<a href="https://msdn.microsoft.com/bbd0d9bc-a463-4cd8-93ee-963dcee8efa6">ConfigurableItem</a> object.


## -parameters




### -param Context [out]

A pointer to a location in memory with the context of a configurable item listed in the context column of the 
<a href="https://msdn.microsoft.com/3b77cc23-c104-4adc-868c-3aa2b5794bc7">ModuleConfiguration table</a>. The client must free the <b>BSTR</b> when it is no longer needed.


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




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

