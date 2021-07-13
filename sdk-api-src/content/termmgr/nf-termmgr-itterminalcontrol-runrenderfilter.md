---
UID: NF:termmgr.ITTerminalControl.RunRenderFilter
title: ITTerminalControl::RunRenderFilter (termmgr.h)
description: The RunRenderFilter method starts the rightmost render filter in the terminal. Needed for dynamic filter graphs.
helpviewer_keywords: ["ITTerminalControl interface [TAPI 2.2]","RunRenderFilter method","ITTerminalControl.RunRenderFilter","ITTerminalControl::RunRenderFilter","RunRenderFilter","RunRenderFilter method [TAPI 2.2]","RunRenderFilter method [TAPI 2.2]","ITTerminalControl interface","_tapi3_itterminalcontrol_runrenderfilter","tapi3.itterminalcontrol_runrenderfilter","termmgr/ITTerminalControl::RunRenderFilter"]
old-location: tapi3\itterminalcontrol_runrenderfilter.htm
tech.root: tapi3
ms.assetid: ed02ed04-3665-47be-a77b-7804a2197767
ms.date: 12/05/2018
ms.keywords: ITTerminalControl interface [TAPI 2.2],RunRenderFilter method, ITTerminalControl.RunRenderFilter, ITTerminalControl::RunRenderFilter, RunRenderFilter, RunRenderFilter method [TAPI 2.2], RunRenderFilter method [TAPI 2.2],ITTerminalControl interface, _tapi3_itterminalcontrol_runrenderfilter, tapi3.itterminalcontrol_runrenderfilter, termmgr/ITTerminalControl::RunRenderFilter
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
 - ITTerminalControl::RunRenderFilter
 - termmgr/ITTerminalControl::RunRenderFilter
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
 - ITTerminalControl.RunRenderFilter
---

# ITTerminalControl::RunRenderFilter


## -description

The 
<b>RunRenderFilter</b> method starts the rightmost render filter in the terminal. Needed for dynamic filter graphs.



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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method not implemented.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itterminalcontrol">ITTerminalControl</a>
