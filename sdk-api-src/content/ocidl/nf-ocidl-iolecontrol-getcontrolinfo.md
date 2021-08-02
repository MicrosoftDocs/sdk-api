---
UID: NF:ocidl.IOleControl.GetControlInfo
title: IOleControl::GetControlInfo (ocidl.h)
description: Retrieves information about the control's keyboard mnemonics and behavior.
helpviewer_keywords: ["GetControlInfo","GetControlInfo method [COM]","GetControlInfo method [COM]","IOleControl interface","IOleControl interface [COM]","GetControlInfo method","IOleControl.GetControlInfo","IOleControl::GetControlInfo","_ctrl_iolecontrol_getcontrolinfo","com.iolecontrol_getcontrolinfo","ocidl/IOleControl::GetControlInfo"]
old-location: com\iolecontrol_getcontrolinfo.htm
tech.root: com
ms.assetid: defb7509-e586-45a0-9e56-de9eba17f18e
ms.date: 12/05/2018
ms.keywords: GetControlInfo, GetControlInfo method [COM], GetControlInfo method [COM],IOleControl interface, IOleControl interface [COM],GetControlInfo method, IOleControl.GetControlInfo, IOleControl::GetControlInfo, _ctrl_iolecontrol_getcontrolinfo, com.iolecontrol_getcontrolinfo, ocidl/IOleControl::GetControlInfo
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
 - IOleControl::GetControlInfo
 - ocidl/IOleControl::GetControlInfo
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
 - IOleControl.GetControlInfo
---

# IOleControl::GetControlInfo


## -description

Retrieves information about the control's keyboard mnemonics and behavior.

## -parameters

### -param pCI [in, out]

A pointer to a <a href="/windows/desktop/api/ocidl/ns-ocidl-controlinfo">CONTROLINFO</a> structure that receives the information.

## -returns

This method can return the standard return value E_OUTOFMEMORY, as well as the following values.

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
The control has no mnemonics.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pCI</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrol">IOleControl</a>