---
UID: NF:tapi3if.ITTerminalSupport2.EnumeratePluggableSuperclasses
title: ITTerminalSupport2::EnumeratePluggableSuperclasses
author: windows-sdk-content
description: The EnumeratePluggableSuperclasses method enumerates the pluggable terminal superclasses registered on the current system.
old-location: tapi3\itterminalsupport2_enumeratepluggablesuperclasses.htm
tech.root: tapi
ms.assetid: 5f1e8490-1b26-45e6-9f9a-e7ddcc840e90
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: EnumeratePluggableSuperclasses, EnumeratePluggableSuperclasses method [TAPI 2.2], EnumeratePluggableSuperclasses method [TAPI 2.2],ITTerminalSupport2 interface, ITTerminalSupport2 interface [TAPI 2.2],EnumeratePluggableSuperclasses method, ITTerminalSupport2.EnumeratePluggableSuperclasses, ITTerminalSupport2::EnumeratePluggableSuperclasses, _tapi3_itterminalsupport2_enumeratepluggablesuperclasses, tapi3.itterminalsupport2_enumeratepluggablesuperclasses, tapi3if/ITTerminalSupport2::EnumeratePluggableSuperclasses
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
 - ITTerminalSupport2.EnumeratePluggableSuperclasses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalSupport2::EnumeratePluggableSuperclasses


## -description


The 
<b>EnumeratePluggableSuperclasses</b> method enumerates the pluggable terminal superclasses registered on the current system.

This method is intended for Visual Basic and scripting applications. C/C++ applications must use the 
<a href="https://msdn.microsoft.com/6d66aeca-5ac2-4019-b326-71c3bfb6d28e">get_PluggableSuperClasses</a> method.


## -parameters




### -param ppSuperclassEnumerator [out]

Pointer to the 
<a href="https://msdn.microsoft.com/80b84976-4256-47d2-a965-3ebe89a3821a">IEnumPluggableSuperclassInfo</a> interface.


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
The <i>ppSuperclassEnumerator</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/80b84976-4256-47d2-a965-3ebe89a3821a">IEnumPluggableSuperclassInfo</a> interface returned by <b>ITTerminalSupport2::EnumeratePluggableSuperclasses</b>. The application must call <a href="_com_iunknown_release">Release</a> on the 
<b>IEnumPluggableSuperclassInfo</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/80b84976-4256-47d2-a965-3ebe89a3821a">IEnumPluggableSuperclassInfo</a>



<a href="https://msdn.microsoft.com/58611991-746c-4626-a1b1-535a2134ee27">ITTerminalSupport2</a>
 

 

