---
UID: NN:termmgr.ITPluggableTerminalInitialization
title: ITPluggableTerminalInitialization (termmgr.h)
description: The ITPluggableTerminalInitialization interface is implemented by pluggable terminals and allows the Terminal Manager to initialize the terminal. The ITPluggableTerminalInitialization interface is created by calling QueryInterface on ITTerminal.
old-location: tapi3\itpluggableterminalinitialization.htm
tech.root: Tapi
ms.assetid: cc1e6fb7-1b2a-40bd-83a8-d3b8be93ddc0
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalInitialization, ITPluggableTerminalInitialization interface [TAPI 2.2], ITPluggableTerminalInitialization interface [TAPI 2.2],described, _tapi3_itpluggableterminalinitialization, tapi3.itpluggableterminalinitialization, termmgr/ITPluggableTerminalInitialization
ms.topic: interface
f1_keywords:
- termmgr/ITPluggableTerminalInitialization
dev_langs:
- c++
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITPluggableTerminalInitialization
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalInitialization interface


## -description


The 
<b>ITPluggableTerminalInitialization</b> interface is implemented by pluggable terminals and allows the Terminal Manager to initialize the terminal. The 
<b>ITPluggableTerminalInitialization</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalInitialization</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPluggableTerminalInitialization</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalinitialization-initializedynamic">InitializeDynamic</a>
</td>
<td align="left" width="63%">
Performs primary terminal object creation for the pluggable terminal.

</td>
</tr>
</table> 

