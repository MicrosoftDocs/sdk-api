---
UID: NN:termmgr.ITPluggableTerminalInitialization
title: ITPluggableTerminalInitialization
author: windows-sdk-content
description: The ITPluggableTerminalInitialization interface is implemented by pluggable terminals and allows the Terminal Manager to initialize the terminal. The ITPluggableTerminalInitialization interface is created by calling QueryInterface on ITTerminal.
old-location: tapi3\itpluggableterminalinitialization.htm
old-project: tapi
ms.assetid: cc1e6fb7-1b2a-40bd-83a8-d3b8be93ddc0
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITPluggableTerminalInitialization, ITPluggableTerminalInitialization interface [TAPI 2.2], ITPluggableTerminalInitialization interface [TAPI 2.2],described, _tapi3_itpluggableterminalinitialization, tapi3.itpluggableterminalinitialization, termmgr/ITPluggableTerminalInitialization
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
 - Tapi3.dll
api_name:
 - ITPluggableTerminalInitialization
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalInitialization interface


## -description


The 
<b>ITPluggableTerminalInitialization</b> interface is implemented by pluggable terminals and allows the Terminal Manager to initialize the terminal. The 
<b>ITPluggableTerminalInitialization</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalInitialization</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITPluggableTerminalInitialization</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPluggableTerminalInitialization</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cda6540-0c27-4234-8b7e-ffff117903b8">InitializeDynamic</a>
</td>
<td align="left" width="63%">
Performs primary terminal object creation for the pluggable terminal.

</td>
</tr>
</table> 

