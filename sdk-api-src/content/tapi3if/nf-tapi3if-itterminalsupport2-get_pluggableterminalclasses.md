---
UID: NF:tapi3if.ITTerminalSupport2.get_PluggableTerminalClasses
title: ITTerminalSupport2::get_PluggableTerminalClasses
author: windows-sdk-content
description: The get_PluggableTerminalClasses method returns a collection of ITPluggableTerminalClassInfo terminal class information interface pointers.
old-location: tapi3\itterminalsupport2_get_pluggableterminalclasses.htm
tech.root: tapi
ms.assetid: 4bbb7f77-fc67-4b6b-88fa-2dc5bcfb6c48
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITTerminalSupport2 interface [TAPI 2.2],get_PluggableTerminalClasses method, ITTerminalSupport2.get_PluggableTerminalClasses, ITTerminalSupport2::get_PluggableTerminalClasses, _tapi3_itterminalsupport2_get_pluggableterminalclasses, get_PluggableTerminalClasses, get_PluggableTerminalClasses method [TAPI 2.2], get_PluggableTerminalClasses method [TAPI 2.2],ITTerminalSupport2 interface, tapi3.itterminalsupport2_get_pluggableterminalclasses, tapi3if/ITTerminalSupport2::get_PluggableTerminalClasses
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminalSupport2.get_PluggableTerminalClasses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITTerminalSupport2.get_PluggableTerminalClasses
: 
---

# ITTerminalSupport2::get_PluggableTerminalClasses


## -description


The 
<b>get_PluggableTerminalClasses</b> method returns a collection of 
<a href="https://msdn.microsoft.com/0f7190c4-c696-4749-82f2-20fdbc8651f4">ITPluggableTerminalClassInfo</a> terminal class information interface pointers.

This method is intended for Visual Basic and scripting applications. C/C++ applications can use the 
<a href="https://msdn.microsoft.com/e8a10b1b-b08e-49b2-bfc6-9f8f4dbc1248">EnumeratePluggableTerminalClasses</a> method.


## -parameters




### -param bstrTerminalSuperclass [in]

The <b>BSTR</b> representation of the CLSID for the terminal superclass.


### -param lMediaType [in]

Bitwise ORed list of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a> supported by the terminal classes.


### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/0f7190c4-c696-4749-82f2-20fdbc8651f4">ITPluggableTerminalClassInfo</a> interface pointers.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not valid.

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
The <i>bstrTerminalSuperclass</i> or <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/0f7190c4-c696-4749-82f2-20fdbc8651f4">ITPluggableTerminalClassInfo</a> interface returned by <b>ITTerminalSupport2::get_PluggableTerminalClasses</b>. The application must call <a href="_com_iunknown_release">Release</a> on the 
<b>ITPluggableTerminalClassInfo</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/0f7190c4-c696-4749-82f2-20fdbc8651f4">ITPluggableTerminalClassInfo</a>



<a href="https://msdn.microsoft.com/58611991-746c-4626-a1b1-535a2134ee27">ITTerminalSupport2</a>
 

 

