---
UID: NF:ntmsapi.IdentifyNtmsSlot
title: IdentifyNtmsSlot function (ntmsapi.h)
description: The IdentifyNtmsSlot function identifies the media in the specified slot in a library. The command returns when the identification is complete.
helpviewer_keywords: ["IdentifyNtmsSlot","IdentifyNtmsSlot function [Files]","NTMS_DISMOUNT_DEFERRED","NTMS_DISMOUNT_IMMEDIATE","_zaw_identifyntmsslot","base.identifyntmsslot","fs.identifyntmsslot","ntmsapi/IdentifyNtmsSlot"]
old-location: fs\identifyntmsslot.htm
tech.root: fs
ms.assetid: 8fdddce9-34fa-4223-b55e-17620db9bbfc
ms.date: 12/05/2018
ms.keywords: IdentifyNtmsSlot, IdentifyNtmsSlot function [Files], NTMS_DISMOUNT_DEFERRED, NTMS_DISMOUNT_IMMEDIATE, _zaw_identifyntmsslot, base.identifyntmsslot, fs.identifyntmsslot, ntmsapi/IdentifyNtmsSlot
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IdentifyNtmsSlot
 - ntmsapi/IdentifyNtmsSlot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - IdentifyNtmsSlot
---

# IdentifyNtmsSlot function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>IdentifyNtmsSlot</b> function identifies the media in the specified slot in a library. The command returns when the identification is complete.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpSlotId [in]

Unique identifier of the slot object to be identified.

### -param dwOption [in]

This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_DISMOUNT_DEFERRED"></a><a id="ntms_dismount_deferred"></a><dl>
<dt><b>NTMS_DISMOUNT_DEFERRED</b></dt>
</dl>
</td>
<td width="60%">
Leave the media in the drive after the media identification is complete, as if it had been dismounted with the "deferred" option.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DISMOUNT_IMMEDIATE"></a><a id="ntms_dismount_immediate"></a><dl>
<dt><b>NTMS_DISMOUNT_IMMEDIATE</b></dt>
</dl>
</td>
<td width="60%">
Dismount the media in the drive after the media identification is complete.

</td>
</tr>
</table>

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access to one or more RSM objects is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The slot ID or the <i>dwOption</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>

## -remarks

If the slot is empty the function returns ERROR_SUCCESS, but no new media records appear.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-inventoryntmslibrary">InventoryNtmsLibrary</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>