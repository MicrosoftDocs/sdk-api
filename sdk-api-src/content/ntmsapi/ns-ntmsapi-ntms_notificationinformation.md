---
UID: NS:ntmsapi._NTMS_NOTIFICATIONINFORMATION
title: NTMS_NOTIFICATIONINFORMATION (ntmsapi.h)
description: The NTMS_NOTIFICATIONINFORMATION structure defines an object and operation that occurred in the RSM database.
helpviewer_keywords: ["*LPNTMS_NOTIFICATIONINFORMATION","LPNTMS_NOTIFICATIONINFORMATION","LPNTMS_NOTIFICATIONINFORMATION structure pointer [Files]","NTMS_NOTIFICATIONINFORMATION","NTMS_NOTIFICATIONINFORMATION structure [Files]","NTMS_OBJ_DELETE","NTMS_OBJ_INSERT","NTMS_OBJ_UPDATE","_zaw_ntms_notificationinformation","base.ntms_notificationinformation","fs.ntms_notificationinformation","ntmsapi/LPNTMS_NOTIFICATIONINFORMATION","ntmsapi/NTMS_NOTIFICATIONINFORMATION"]
old-location: fs\ntms_notificationinformation.htm
tech.root: fs
ms.assetid: d9c6904b-260d-4598-9575-49c7d7b6e66d
ms.date: 12/05/2018
ms.keywords: '*LPNTMS_NOTIFICATIONINFORMATION, LPNTMS_NOTIFICATIONINFORMATION, LPNTMS_NOTIFICATIONINFORMATION structure pointer [Files], NTMS_NOTIFICATIONINFORMATION, NTMS_NOTIFICATIONINFORMATION structure [Files], NTMS_OBJ_DELETE, NTMS_OBJ_INSERT, NTMS_OBJ_UPDATE, _zaw_ntms_notificationinformation, base.ntms_notificationinformation, fs.ntms_notificationinformation, ntmsapi/LPNTMS_NOTIFICATIONINFORMATION, ntmsapi/NTMS_NOTIFICATIONINFORMATION'
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
req.typenames: NTMS_NOTIFICATIONINFORMATION, *LPNTMS_NOTIFICATIONINFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_NOTIFICATIONINFORMATION
 - ntmsapi/_NTMS_NOTIFICATIONINFORMATION
 - LPNTMS_NOTIFICATIONINFORMATION
 - ntmsapi/LPNTMS_NOTIFICATIONINFORMATION
 - NTMS_NOTIFICATIONINFORMATION
 - ntmsapi/NTMS_NOTIFICATIONINFORMATION
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
 - NTMS_NOTIFICATIONINFORMATION
---

# NTMS_NOTIFICATIONINFORMATION structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_NOTIFICATIONINFORMATION</b> structure defines an object and operation that occurred in the RSM database.

## -struct-fields

### -field dwOperation

Operation that occurred on the object. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_OBJ_INSERT"></a><a id="ntms_obj_insert"></a><dl>
<dt><b>NTMS_OBJ_INSERT</b></dt>
</dl>
</td>
<td width="60%">
New object was inserted.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OBJ_DELETE"></a><a id="ntms_obj_delete"></a><dl>
<dt><b>NTMS_OBJ_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Object was deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OBJ_UPDATE"></a><a id="ntms_obj_update"></a><dl>
<dt><b>NTMS_OBJ_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Object was updated.

</td>
</tr>
</table>

### -field ObjectId

Object Identifier.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-waitforntmsnotification">WaitForNtmsNotification</a>