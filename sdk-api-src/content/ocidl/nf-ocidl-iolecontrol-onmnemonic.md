---
UID: NF:ocidl.IOleControl.OnMnemonic
title: IOleControl::OnMnemonic (ocidl.h)
description: Informs a control that the user has pressed a keystroke that represents a keyboard mnemonic.
helpviewer_keywords: ["IOleControl interface [COM]","OnMnemonic method","IOleControl.OnMnemonic","IOleControl::OnMnemonic","OnMnemonic","OnMnemonic method [COM]","OnMnemonic method [COM]","IOleControl interface","_ctrl_iolecontrol_onmnemonic","com.iolecontrol_onmnemonic","ocidl/IOleControl::OnMnemonic"]
old-location: com\iolecontrol_onmnemonic.htm
tech.root: com
ms.assetid: 3b40afc9-89cf-4dfc-ab25-055bdf6964ce
ms.date: 12/05/2018
ms.keywords: IOleControl interface [COM],OnMnemonic method, IOleControl.OnMnemonic, IOleControl::OnMnemonic, OnMnemonic, OnMnemonic method [COM], OnMnemonic method [COM],IOleControl interface, _ctrl_iolecontrol_onmnemonic, com.iolecontrol_onmnemonic, ocidl/IOleControl::OnMnemonic
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IOleControl::OnMnemonic
 - ocidl/IOleControl::OnMnemonic
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleControl.OnMnemonic
---

# IOleControl::OnMnemonic


## -description

Informs a control that the user has pressed a keystroke that represents a keyboard mnemonic.

## -parameters

### -param pMsg [in]

A pointer to the <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure describing the keystroke to be processed.

## -returns

This method can return the standard return values E_INVALIDARG and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The control does not handle mnemonics. This indicates an unexpected condition and a caller error. For example, the caller has mismatched which control has which mnemonic.

</td>
</tr>
</table>

## -remarks

The keystroke must match one of the <b>ACCEL</b> entries in the mnemonic table returned through <a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrol-getcontrolinfo">IOleControl::GetControlInfo</a>. The control takes whatever action is appropriate for the keystroke.


<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
 A container of a control is allowed to cache the control's <a href="/windows/desktop/api/ocidl/ns-ocidl-controlinfo">CONTROLINFO</a> structure, provided that the container implements <a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-oncontrolinfochanged">IOleControlSite::OnControlInfoChanged</a> to know when it must update its cached information.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If a control changes the contents of its <a href="/windows/desktop/api/ocidl/ns-ocidl-controlinfo">CONTROLINFO</a> structure, it must notify its container by calling <a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-oncontrolinfochanged">IOleControlSite::OnControlInfoChanged</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrol">IOleControl</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-oncontrolinfochanged">IOleControlSite::OnControlInfoChanged</a>