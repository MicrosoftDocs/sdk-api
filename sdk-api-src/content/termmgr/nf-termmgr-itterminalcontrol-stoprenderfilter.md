---
UID: NF:termmgr.ITTerminalControl.StopRenderFilter
title: ITTerminalControl::StopRenderFilter (termmgr.h)
description: The StopRenderFilter method stops the rightmost render filter in the terminal. Needed for dynamic filter graphs.
helpviewer_keywords: ["ITTerminalControl interface [TAPI 2.2]","StopRenderFilter method","ITTerminalControl.StopRenderFilter","ITTerminalControl::StopRenderFilter","StopRenderFilter","StopRenderFilter method [TAPI 2.2]","StopRenderFilter method [TAPI 2.2]","ITTerminalControl interface","_tapi3_itterminalcontrol_stoprenderfilter","tapi3.itterminalcontrol_stoprenderfilter","termmgr/ITTerminalControl::StopRenderFilter"]
old-location: tapi3\itterminalcontrol_stoprenderfilter.htm
tech.root: tapi3
ms.assetid: 30a47de7-c54d-4600-9b4b-07013f962c4d
ms.date: 12/05/2018
ms.keywords: ITTerminalControl interface [TAPI 2.2],StopRenderFilter method, ITTerminalControl.StopRenderFilter, ITTerminalControl::StopRenderFilter, StopRenderFilter, StopRenderFilter method [TAPI 2.2], StopRenderFilter method [TAPI 2.2],ITTerminalControl interface, _tapi3_itterminalcontrol_stoprenderfilter, tapi3.itterminalcontrol_stoprenderfilter, termmgr/ITTerminalControl::StopRenderFilter
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
 - ITTerminalControl::StopRenderFilter
 - termmgr/ITTerminalControl::StopRenderFilter
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
 - ITTerminalControl.StopRenderFilter
---

# ITTerminalControl::StopRenderFilter


## -description

The 
<b>StopRenderFilter</b> method stops the rightmost render filter in the terminal. Needed for dynamic filter graphs.



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
