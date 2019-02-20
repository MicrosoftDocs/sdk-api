---
UID: NF:mergemod.IMsmConfigurableItem.get_Context
title: IMsmConfigurableItem::get_Context
author: windows-sdk-content
description: The get_Context method retrieves the Context property of the ConfigurableItem object.
old-location: setup\imsmconfigurableitem_get_context.htm
tech.root: Msi
ms.assetid: 90aa0ee2-a7eb-464c-8a8f-ed4bdf46990e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMsmConfigurableItem interface,get_Context method, IMsmConfigurableItem.get_Context, IMsmConfigurableItem::get_Context, _msi_get_context_function, get_Context, get_Context method, get_Context method,IMsmConfigurableItem interface, mergemod/IMsmConfigurableItem::get_Context, setup.imsmconfigurableitem_get_context
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
 - IMsmConfigurableItem.get_Context
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmConfigurableItem::get_Context


## -description


The 
<b>get_Context</b> method retrieves the 
<a href="https://msdn.microsoft.com/27b94142-81cb-4ea7-aa73-c359cb50ce71">Context</a> property of the 
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




<a href="https://msdn.microsoft.com/d10bfd31-22a8-4100-ac0b-dd0795622808">IMsmConfigurableItem</a>



<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

