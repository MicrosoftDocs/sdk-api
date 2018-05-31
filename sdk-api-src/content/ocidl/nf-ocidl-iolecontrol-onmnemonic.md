---
UID: NF:ocidl.IOleControl.OnMnemonic
title: IOleControl::OnMnemonic
author: windows-sdk-content
description: Informs a control that the user has pressed a keystroke that represents a keyboard mneumonic.
old-location: com\iolecontrol_onmnemonic.htm
old-project: com
ms.assetid: 3b40afc9-89cf-4dfc-ab25-055bdf6964ce
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IOleControl interface [COM],OnMnemonic method, IOleControl.OnMnemonic, IOleControl::OnMnemonic, OnMnemonic, OnMnemonic method [COM], OnMnemonic method [COM],IOleControl interface, _ctrl_iolecontrol_onmnemonic, com.iolecontrol_onmnemonic, ocidl/IOleControl::OnMnemonic
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IOleControl.OnMnemonic
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleControl::OnMnemonic


## -description


Informs a control that the user has pressed a keystroke that represents a keyboard mneumonic.


## -parameters




### -param pMsg [in]

A pointer to the <a href="_win32_MSG_str_cpp">MSG</a> structure describing the keystroke to be processed.


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



The keystroke must match one of the <b>ACCEL</b> entries in the mnemonic table returned through <a href="https://msdn.microsoft.com/defb7509-e586-45a0-9e56-de9eba17f18e">IOleControl::GetControlInfo</a>. The control takes whatever action is appropriate for the keystroke.


<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
 A container of a control is allowed to cache the control's <a href="https://msdn.microsoft.com/3f22dc1d-554a-4dd1-a79a-121117f65caf">CONTROLINFO</a> structure, provided that the container implements <a href="https://msdn.microsoft.com/d9e915c0-3443-4464-9e3e-e1fbfe37e838">IOleControlSite::OnControlInfoChanged</a> to know when it must update its cached information.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If a control changes the contents of its <a href="https://msdn.microsoft.com/3f22dc1d-554a-4dd1-a79a-121117f65caf">CONTROLINFO</a> structure, it must notify its container by calling <a href="https://msdn.microsoft.com/d9e915c0-3443-4464-9e3e-e1fbfe37e838">IOleControlSite::OnControlInfoChanged</a>.




## -see-also




<a href="https://msdn.microsoft.com/ef85dce6-b680-4a72-9277-4cfdab27cbbc">IOleControl</a>



<a href="https://msdn.microsoft.com/d9e915c0-3443-4464-9e3e-e1fbfe37e838">IOleControlSite::OnControlInfoChanged</a>
 

 

