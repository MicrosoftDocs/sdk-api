---
UID: NS:ntmsapi._NTMS_IEDOORINFORMATION
title: NTMS_IEDOORINFORMATION (ntmsapi.h)
description: The NTMS_IEDOORINFORMATION structure defines properties specific to an insert/eject door object.
helpviewer_keywords: ["NTMS_DOORSTATE_CLOSED","NTMS_DOORSTATE_OPEN","NTMS_DOORSTATE_UNKNOWN","NTMS_IEDOORINFORMATION","NTMS_IEDOORINFORMATION structure [Files]","_zaw_ntms_iedoorinformation","base.ntms_iedoorinformation","fs.ntms_iedoorinformation","ntmsapi/NTMS_IEDOORINFORMATION"]
old-location: fs\ntms_iedoorinformation.htm
tech.root: fs
ms.assetid: a0619420-f391-4695-a87e-8cbf8d3a3742
ms.date: 12/05/2018
ms.keywords: NTMS_DOORSTATE_CLOSED, NTMS_DOORSTATE_OPEN, NTMS_DOORSTATE_UNKNOWN, NTMS_IEDOORINFORMATION, NTMS_IEDOORINFORMATION structure [Files], _zaw_ntms_iedoorinformation, base.ntms_iedoorinformation, fs.ntms_iedoorinformation, ntmsapi/NTMS_IEDOORINFORMATION
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: NTMS_IEDOORINFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_IEDOORINFORMATION
 - ntmsapi/_NTMS_IEDOORINFORMATION
 - NTMS_IEDOORINFORMATION
 - ntmsapi/NTMS_IEDOORINFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntmsapi.h
api_name:
 - NTMS_IEDOORINFORMATION
---

# NTMS_IEDOORINFORMATION structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_IEDOORINFORMATION</b> structure defines properties specific to an insert/eject door object.

## -struct-fields

### -field Number

Number of the door in the library. Typically, libraries have one door.

### -field State

State of the door. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_DOORSTATE_CLOSED"></a><a id="ntms_doorstate_closed"></a><dl>
<dt><b>NTMS_DOORSTATE_CLOSED</b></dt>
</dl>
</td>
<td width="60%">
Library door is closed.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DOORSTATE_OPEN"></a><a id="ntms_doorstate_open"></a><dl>
<dt><b>NTMS_DOORSTATE_OPEN</b></dt>
</dl>
</td>
<td width="60%">
Library door is open.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DOORSTATE_UNKNOWN"></a><a id="ntms_doorstate_unknown"></a><dl>
<dt><b>NTMS_DOORSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
State of the library is unknown.

</td>
</tr>
</table>

### -field MaxOpenSecs

Maximum number of seconds the door is to remain open. Valid values are between 0-65,535 seconds This member is writable.

### -field Library

Library that contains this door.

## -remarks

The 
<b>NTMS_IEDOORINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.

If the <b>MaxOpenSecs</b> member is zero, an operator request to close the door is generated as soon as the door is open.

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>