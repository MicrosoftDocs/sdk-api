---
UID: NN:tapi3if.ITTerminalSupport2
title: ITTerminalSupport2
author: windows-sdk-content
description: The ITTerminalSupport2 interface is derived from the ITTerminalSupport interface. ITTerminalSupport2 supports the retrieval of information about pluggable terminal classes and superclasses by C, C++, and scripting applications.
old-location: tapi3\itterminalsupport2.htm
tech.root: Tapi
ms.assetid: 58611991-746c-4626-a1b1-535a2134ee27
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITTerminalSupport2, ITTerminalSupport2 interface [TAPI 2.2], ITTerminalSupport2 interface [TAPI 2.2],described, _tapi3_itterminalsupport2, tapi3.itterminalsupport2, tapi3if/ITTerminalSupport2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ITTerminalSupport2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalSupport2 interface


## -description


The 
<b>ITTerminalSupport2</b> interface is derived from the 
<a href="https://msdn.microsoft.com/8669324a-5c2c-4ed8-be24-a0c71fbb8c01">ITTerminalSupport</a> interface. 
<b>ITTerminalSupport2</b> supports the retrieval of information about pluggable terminal classes and superclasses by C, C++, and scripting applications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTerminalSupport2</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITTerminalSupport2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTerminalSupport2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f1e8490-1b26-45e6-9f9a-e7ddcc840e90">EnumeratePluggableSuperclasses</a>
</td>
<td align="left" width="63%">
Gets an 
<a href="https://msdn.microsoft.com/80b84976-4256-47d2-a965-3ebe89a3821a">IEnumPluggableSuperclassInfo</a> enumeration of pluggable terminal superclasses registered on the current system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8a10b1b-b08e-49b2-bfc6-9f8f4dbc1248">EnumeratePluggableTerminalClasses</a>
</td>
<td align="left" width="63%">
Gets an 
<a href="https://msdn.microsoft.com/72c0db41-8391-4923-8961-6aefce9886c4">IEnumPluggableTerminalClassInfo</a> enumeration of the pluggable terminal classes registered under a given superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d66aeca-5ac2-4019-b326-71c3bfb6d28e">get_PluggableSuperclasses</a>
</td>
<td align="left" width="63%">
Gets a collection of 
<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a> superclass information interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bbb7f77-fc67-4b6b-88fa-2dc5bcfb6c48">get_PluggableTerminalClasses</a>
</td>
<td align="left" width="63%">
Gets a collection of 
<a href="https://msdn.microsoft.com/0f7190c4-c696-4749-82f2-20fdbc8651f4">ITPluggableTerminalClassInfo</a> terminal class information interfaces.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/80b84976-4256-47d2-a965-3ebe89a3821a">IEnumPluggableSuperclassInfo</a>



<a href="https://msdn.microsoft.com/72c0db41-8391-4923-8961-6aefce9886c4">IEnumPluggableTerminalClassInfo</a>



<a href="https://msdn.microsoft.com/0f7190c4-c696-4749-82f2-20fdbc8651f4">ITPluggableTerminalClassInfo</a>



<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a>



<a href="https://msdn.microsoft.com/8669324a-5c2c-4ed8-be24-a0c71fbb8c01">ITTerminalSupport</a>
 

 

