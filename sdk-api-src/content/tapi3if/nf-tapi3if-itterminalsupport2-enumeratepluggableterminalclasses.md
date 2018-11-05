---
UID: NF:tapi3if.ITTerminalSupport2.EnumeratePluggableTerminalClasses
title: ITTerminalSupport2::EnumeratePluggableTerminalClasses
author: windows-sdk-content
description: The EnumeratePluggableTerminalClasses method enumerates the pluggable terminal classes registered under a given superclass.
old-location: tapi3\itterminalsupport2_enumeratepluggableterminalclasses.htm
tech.root: tapi
ms.assetid: e8a10b1b-b08e-49b2-bfc6-9f8f4dbc1248
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EnumeratePluggableTerminalClasses, EnumeratePluggableTerminalClasses method [TAPI 2.2], EnumeratePluggableTerminalClasses method [TAPI 2.2],ITTerminalSupport2 interface, ITTerminalSupport2 interface [TAPI 2.2],EnumeratePluggableTerminalClasses method, ITTerminalSupport2.EnumeratePluggableTerminalClasses, ITTerminalSupport2::EnumeratePluggableTerminalClasses, _tapi3_itterminalsupport2_enumeratepluggableterminalclasses, tapi3.itterminalsupport2_enumeratepluggableterminalclasses, tapi3if/ITTerminalSupport2::EnumeratePluggableTerminalClasses
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
 - ITTerminalSupport2.EnumeratePluggableTerminalClasses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalSupport2::EnumeratePluggableTerminalClasses


## -description


The 
<b>EnumeratePluggableTerminalClasses</b> method enumerates the pluggable terminal classes registered under a given superclass.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="https://msdn.microsoft.com/4bbb7f77-fc67-4b6b-88fa-2dc5bcfb6c48">get_PluggableTerminalClasses</a> method.


## -parameters




### -param iidTerminalSuperclass [in]

CLSID for the terminal superclass.


### -param lMediaType [in]

Bitwise ORed list of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a> supported by the terminal classes.


### -param ppClassEnumerator [out]

Pointer to the 
<a href="https://msdn.microsoft.com/72c0db41-8391-4923-8961-6aefce9886c4">IEnumPluggableTerminalClassInfo</a> interface.


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
The <i>ppClassEnumerator</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/72c0db41-8391-4923-8961-6aefce9886c4">IEnumPluggableTerminalClassInfo</a> interface returned by <b>ITTerminalSupport2::EnumeratePluggableTerminalClasses</b>. The application must call <a href="_com_iunknown_release">Release</a> on the 
<b>IEnumPluggableTerminalClassInfo</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/72c0db41-8391-4923-8961-6aefce9886c4">IEnumPluggableTerminalClassInfo</a>



<a href="https://msdn.microsoft.com/58611991-746c-4626-a1b1-535a2134ee27">ITTerminalSupport2</a>
 

 

