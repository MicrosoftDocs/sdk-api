---
UID: NF:ocidl.IOleControlSite.GetExtendedControl
title: IOleControlSite::GetExtendedControl (ocidl.h)
description: Retrieves an IDispatch pointer to the extended control that the container uses to wrap the real control.
helpviewer_keywords: ["GetExtendedControl","GetExtendedControl method [COM]","GetExtendedControl method [COM]","IOleControlSite interface","IOleControlSite interface [COM]","GetExtendedControl method","IOleControlSite.GetExtendedControl","IOleControlSite::GetExtendedControl","_ctrl_iolecontrolsite_getextendedcontrol","com.iolecontrolsite_getextendedcontrol","ocidl/IOleControlSite::GetExtendedControl"]
old-location: com\iolecontrolsite_getextendedcontrol.htm
tech.root: com
ms.assetid: 66cfdf22-db2b-41d2-9854-d6bf70fbe146
ms.date: 12/05/2018
ms.keywords: GetExtendedControl, GetExtendedControl method [COM], GetExtendedControl method [COM],IOleControlSite interface, IOleControlSite interface [COM],GetExtendedControl method, IOleControlSite.GetExtendedControl, IOleControlSite::GetExtendedControl, _ctrl_iolecontrolsite_getextendedcontrol, com.iolecontrolsite_getextendedcontrol, ocidl/IOleControlSite::GetExtendedControl
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
 - IOleControlSite::GetExtendedControl
 - ocidl/IOleControlSite::GetExtendedControl
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
 - IOleControlSite.GetExtendedControl
---

# IOleControlSite::GetExtendedControl


## -description

Retrieves an <b>IDispatch</b> pointer to the extended control that the container uses to wrap the real control.

## -parameters

### -param ppDisp [out]

A pointer to an <b>IDispatch</b> pointer variable that receives the interface pointer to the extended control. If an error occurs, the implementation must set *<i>ppDisp</i> to <b>NULL</b>. On success, the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when *<i>ppDisp</i> is no longer needed.

## -returns

This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The container does not implement extended controls.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppDisp</i> or *<i>ppDisp</i> is not valid. For example, it may be <b>NULL</b>.


</td>
</tr>
</table>

## -remarks

This method gives the real control access to whatever properties and methods the container maintains in the extended control. These properties and methods would otherwise be inaccessible to the control.



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The returned pointer is the responsibility of the caller, which must release it when it is no longer needed.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a>