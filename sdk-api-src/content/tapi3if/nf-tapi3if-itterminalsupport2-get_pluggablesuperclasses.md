---
UID: NF:tapi3if.ITTerminalSupport2.get_PluggableSuperclasses
title: ITTerminalSupport2::get_PluggableSuperclasses
author: windows-sdk-content
description: The get_PluggableSuperclasses method returns a collection of ITPluggableTerminalSuperclassInfo superclass information interface pointers.
old-location: tapi3\itterminalsupport2_get_pluggablesuperclasses.htm
old-project: Tapi
ms.assetid: 6d66aeca-5ac2-4019-b326-71c3bfb6d28e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITTerminalSupport2 interface [TAPI 2.2],get_PluggableSuperclasses method, ITTerminalSupport2.get_PluggableSuperclasses, ITTerminalSupport2::get_PluggableSuperclasses, _tapi3_itterminalsupport2_get_pluggablesuperclasses, get_PluggableSuperclasses, get_PluggableSuperclasses method [TAPI 2.2], get_PluggableSuperclasses method [TAPI 2.2],ITTerminalSupport2 interface, tapi3.itterminalsupport2_get_pluggablesuperclasses, tapi3if/ITTerminalSupport2::get_PluggableSuperclasses
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminalSupport2.get_PluggableSuperclasses
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTerminalSupport2::get_PluggableSuperclasses


## -description


The 
<b>get_PluggableSuperclasses</b> method returns a collection of 
<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a> superclass information interface pointers.

This method is intended for Visual Basic and scripting applications. C/C++ applications can use the 
<a href="https://msdn.microsoft.com/5f1e8490-1b26-45e6-9f9a-e7ddcc840e90">EnumeratePluggableSuperclasses</a> method.


## -parameters




### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a> interface pointers.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a> interface returned by <b>ITTerminalSupport2::get_PluggableSuperclasses</b>. The application must call <a href="_com_iunknown_release">Release</a> on the 
<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a>



<a href="https://msdn.microsoft.com/58611991-746c-4626-a1b1-535a2134ee27">ITTerminalSupport2</a>
 

 

