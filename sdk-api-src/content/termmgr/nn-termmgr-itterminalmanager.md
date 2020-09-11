---
UID: NN:termmgr.ITTerminalManager
title: ITTerminalManager (termmgr.h)
description: The ITTerminalManager interface is used by the MSP to create dynamic terminals.
helpviewer_keywords: ["ITTerminalManager","ITTerminalManager interface [TAPI 2.2]","ITTerminalManager interface [TAPI 2.2]","described","_tapi3_itterminalmanager","tapi3.itterminalmanager","termmgr/ITTerminalManager"]
old-location: tapi3\itterminalmanager.htm
tech.root: tapi3
ms.assetid: 7e5bd83d-42c5-463c-8ce0-c6f466f60588
ms.date: 12/05/2018
ms.keywords: ITTerminalManager, ITTerminalManager interface [TAPI 2.2], ITTerminalManager interface [TAPI 2.2],described, _tapi3_itterminalmanager, tapi3.itterminalmanager, termmgr/ITTerminalManager
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITTerminalManager
 - termmgr/ITTerminalManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Termmgr.h
api_name:
 - ITTerminalManager
---

# ITTerminalManager interface


## -description

The 
<b>ITTerminalManager</b> interface is used by the MSP to create dynamic terminals.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itterminalmanager2">ITTerminalManager2</a> interface exposes methods that retrieve information about pluggable terminal classes registered in the current system. 
<b>ITTerminalManager2</b> is derived from the 
<b>ITTerminalManager</b> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTerminalManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTerminalManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itterminalmanager-createdynamicterminal">CreateDynamicTerminal</a>
</td>
<td align="left" width="63%">
Create a dynamic terminal of a specified terminal class, media type, and direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses">GetDynamicTerminalClasses</a>
</td>
<td align="left" width="63%">
Gets list of terminal classes.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itterminalmanager2">ITTerminalManager2</a>

