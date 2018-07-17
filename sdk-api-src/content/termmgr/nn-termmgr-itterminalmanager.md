---
UID: NN:termmgr.ITTerminalManager
title: ITTerminalManager
author: windows-sdk-content
description: The ITTerminalManager interface is used by the MSP to create dynamic terminals.
old-location: tapi3\itterminalmanager.htm
old-project: tapi
ms.assetid: 7e5bd83d-42c5-463c-8ce0-c6f466f60588
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITTerminalManager, ITTerminalManager interface [TAPI 2.2], ITTerminalManager interface [TAPI 2.2],described, _tapi3_itterminalmanager, tapi3.itterminalmanager, termmgr/ITTerminalManager
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
tech.root: 
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Termmgr.h
api_name:
 - ITTerminalManager
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTerminalManager interface


## -description


The 
<b>ITTerminalManager</b> interface is used by the MSP to create dynamic terminals.

The 
<a href="https://msdn.microsoft.com/f91c8684-27f8-4db8-99ff-d5a6cb87a0c2">ITTerminalManager2</a> interface exposes methods that retrieve information about pluggable terminal classes registered in the current system. 
<b>ITTerminalManager2</b> is derived from the 
<b>ITTerminalManager</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTerminalManager</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITTerminalManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTerminalManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6590503-8c95-496d-a35a-1bbb34c728e1">CreateDynamicTerminal</a>
</td>
<td align="left" width="63%">
Create a dynamic terminal of a specified terminal class, media type, and direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e0ae94c-eab9-4ca2-a982-a5673f73130e">GetDynamicTerminalClasses</a>
</td>
<td align="left" width="63%">
Gets list of terminal classes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/f91c8684-27f8-4db8-99ff-d5a6cb87a0c2">ITTerminalManager2</a>
 

 

