---
UID: NF:mergemod.IMsmMerge2.get_ConfigurableItems
title: IMsmMerge2::get_ConfigurableItems
author: windows-sdk-content
description: The get_ConfigurableItems method retrieves the ConfigurableItems property of the Merge object.
old-location: setup\imsmmerge2_get_configurableitems.htm
old-project: Msi
ms.assetid: c8b34ff7-6b0b-4cd9-bcb2-9d0da6b14254
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMsmMerge2 interface,get_ConfigurableItems method, IMsmMerge2.get_ConfigurableItems, IMsmMerge2::get_ConfigurableItems, _msi_get_configurableitems_function, get_ConfigurableItems, get_ConfigurableItems method, get_ConfigurableItems method,IMsmMerge2 interface, mergemod/IMsmMerge2::get_ConfigurableItems, setup.imsmmerge2_get_configurableitems
ms.prod: windows
ms.technology: windows-sdk
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
-	IMsmMerge2.get_ConfigurableItems
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmMerge2::get_ConfigurableItems


## -description


The 
<b>get_ConfigurableItems</b> method retrieves the 
<a href="https://msdn.microsoft.com/4d1a64f7-fbd0-4358-8911-112e43f1be4a">ConfigurableItems</a> property of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object. 


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




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

