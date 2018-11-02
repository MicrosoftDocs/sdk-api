---
UID: NN:termmgr.ITTerminalManager2
title: ITTerminalManager2
author: windows-sdk-content
description: The ITTerminalManager2 interface exposes methods that retrieve information about pluggable terminal classes registered in the current system. ITTerminalManager2 is derived from the ITTerminalManager interface.
old-location: tapi3\itterminalmanager2.htm
tech.root: tapi
ms.assetid: f91c8684-27f8-4db8-99ff-d5a6cb87a0c2
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITTerminalManager2, ITTerminalManager2 interface [TAPI 2.2], ITTerminalManager2 interface [TAPI 2.2],described, _tapi3_itterminalmanager2, tapi3.itterminalmanager2, termmgr/ITTerminalManager2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: termmgr.h
req.include-header: 
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
 - Termmgr.h
api_name:
 - ITTerminalManager2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalManager2 interface


## -description


The 
<b>ITTerminalManager2</b> interface exposes methods that retrieve information about pluggable terminal classes registered in the current system. 
<b>ITTerminalManager2</b> is derived from the 
<a href="https://msdn.microsoft.com/7e5bd83d-42c5-463c-8ce0-c6f466f60588">ITTerminalManager</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTerminalManager2</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITTerminalManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTerminalManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3db1979-0ba5-416a-bb14-0ac4b61eb425">GetPluggableSuperclasses</a>
</td>
<td align="left" width="63%">
Gets the public CLSIDs for all pluggable terminal superclasses in the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f967958-fc32-4336-aae5-bea180ba86d1">GetPluggableTerminalClasses</a>
</td>
<td align="left" width="63%">
Gets the terminal classes for all pluggable terminals registered under a terminal superclass.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/7e5bd83d-42c5-463c-8ce0-c6f466f60588">ITTerminalManager</a>
 

 

