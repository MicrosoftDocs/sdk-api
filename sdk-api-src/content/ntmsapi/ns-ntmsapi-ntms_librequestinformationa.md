---
UID: NS:ntmsapi._NTMS_LIBREQUESTINFORMATIONA
title: NTMS_LIBREQUESTINFORMATIONA (ntmsapi.h)
description: The NTMS_LIBREQUESTINFORMATION structure defines the properties specific to a work request, which are queued to RSM. (ANSI)
helpviewer_keywords: ["NTMS_LIBREQUESTINFORMATION","NTMS_LIBREQUESTINFORMATION structure [Files]","NTMS_LIBREQUESTINFORMATIONA","NTMS_LIBREQUESTINFORMATIONW","NTMS_LM_CANCELLED","NTMS_LM_CLASSIFY","NTMS_LM_CLEANDRIVE","NTMS_LM_DISABLEDRIVE","NTMS_LM_DISABLELIBRARY","NTMS_LM_DISABLEMEDIA","NTMS_LM_DISMOUNT","NTMS_LM_DOORACCESS","NTMS_LM_EJECT","NTMS_LM_EJECTCLEANER","NTMS_LM_ENABLEDRIVE","NTMS_LM_ENABLELIBRARY","NTMS_LM_ENABLEMEDIA","NTMS_LM_FAILED","NTMS_LM_INJECT","NTMS_LM_INJECTCLEANER","NTMS_LM_INPROCESS","NTMS_LM_INVALID","NTMS_LM_INVENTORY","NTMS_LM_MOUNT","NTMS_LM_PASSED","NTMS_LM_PROCESSOMID","NTMS_LM_QUEUED","NTMS_LM_RELEASECLEANER","NTMS_LM_REMOVE","NTMS_LM_RESERVECLEANER","NTMS_LM_UPDATEOMID","NTMS_LM_WAITING","NTMS_LM_WRITESCRATCH","_NTMS_LIBREQUESTINFORMATIONA","_NTMS_LIBREQUESTINFORMATIONW","_zaw_ntms_librequestinformation","base.ntms_librequestinformation","fs.ntms_librequestinformation","ntmsapi/NTMS_LIBREQUESTINFORMATION"]
old-location: fs\ntms_librequestinformation.htm
tech.root: fs
ms.assetid: 0250ed88-410c-4fe3-8188-5e6253d45dc4
ms.date: 12/05/2018
ms.keywords: NTMS_LIBREQUESTINFORMATION, NTMS_LIBREQUESTINFORMATION structure [Files], NTMS_LIBREQUESTINFORMATIONA, NTMS_LIBREQUESTINFORMATIONW, NTMS_LM_CANCELLED, NTMS_LM_CLASSIFY, NTMS_LM_CLEANDRIVE, NTMS_LM_DISABLEDRIVE, NTMS_LM_DISABLELIBRARY, NTMS_LM_DISABLEMEDIA, NTMS_LM_DISMOUNT, NTMS_LM_DOORACCESS, NTMS_LM_EJECT, NTMS_LM_EJECTCLEANER, NTMS_LM_ENABLEDRIVE, NTMS_LM_ENABLELIBRARY, NTMS_LM_ENABLEMEDIA, NTMS_LM_FAILED, NTMS_LM_INJECT, NTMS_LM_INJECTCLEANER, NTMS_LM_INPROCESS, NTMS_LM_INVALID, NTMS_LM_INVENTORY, NTMS_LM_MOUNT, NTMS_LM_PASSED, NTMS_LM_PROCESSOMID, NTMS_LM_QUEUED, NTMS_LM_RELEASECLEANER, NTMS_LM_REMOVE, NTMS_LM_RESERVECLEANER, NTMS_LM_UPDATEOMID, NTMS_LM_WAITING, NTMS_LM_WRITESCRATCH, _NTMS_LIBREQUESTINFORMATIONA, _NTMS_LIBREQUESTINFORMATIONW, _zaw_ntms_librequestinformation, base.ntms_librequestinformation, fs.ntms_librequestinformation, ntmsapi/NTMS_LIBREQUESTINFORMATION
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
req.typenames: NTMS_LIBREQUESTINFORMATIONA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_LIBREQUESTINFORMATIONA
 - ntmsapi/_NTMS_LIBREQUESTINFORMATIONA
 - NTMS_LIBREQUESTINFORMATIONA
 - ntmsapi/NTMS_LIBREQUESTINFORMATIONA
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
 - NTMS_LIBREQUESTINFORMATION
 - NTMS_LIBREQUESTINFORMATIONA
 - NTMS_LIBREQUESTINFORMATIONW
---

# NTMS_LIBREQUESTINFORMATIONA structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_LIBREQUESTINFORMATION</b> structure defines the properties specific to a work request, which are queued to RSM.

## -struct-fields

### -field OperationCode

Item operation. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_CLASSIFY"></a><a id="ntms_lm_classify"></a><dl>
<dt><b>NTMS_LM_CLASSIFY</b></dt>
</dl>
</td>
<td width="60%">
Classify the medium.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_CLEANDRIVE"></a><a id="ntms_lm_cleandrive"></a><dl>
<dt><b>NTMS_LM_CLEANDRIVE</b></dt>
</dl>
</td>
<td width="60%">
Clean a drive.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_DISABLELIBRARY"></a><a id="ntms_lm_disablelibrary"></a><dl>
<dt><b>NTMS_LM_DISABLELIBRARY</b></dt>
</dl>
</td>
<td width="60%">
Disable the changer.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_DISABLEDRIVE"></a><a id="ntms_lm_disabledrive"></a><dl>
<dt><b>NTMS_LM_DISABLEDRIVE</b></dt>
</dl>
</td>
<td width="60%">
Disable a drive.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_DISABLEMEDIA"></a><a id="ntms_lm_disablemedia"></a><dl>
<dt><b>NTMS_LM_DISABLEMEDIA</b></dt>
</dl>
</td>
<td width="60%">
Disable the medium.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_DISMOUNT"></a><a id="ntms_lm_dismount"></a><dl>
<dt><b>NTMS_LM_DISMOUNT</b></dt>
</dl>
</td>
<td width="60%">
Dismount the medium from a drive.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_DOORACCESS"></a><a id="ntms_lm_dooraccess"></a><dl>
<dt><b>NTMS_LM_DOORACCESS</b></dt>
</dl>
</td>
<td width="60%">
Allow access to media through a library unit door.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_EJECT"></a><a id="ntms_lm_eject"></a><dl>
<dt><b>NTMS_LM_EJECT</b></dt>
</dl>
</td>
<td width="60%">
Eject the medium from the library.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_EJECTCLEANER"></a><a id="ntms_lm_ejectcleaner"></a><dl>
<dt><b>NTMS_LM_EJECTCLEANER</b></dt>
</dl>
</td>
<td width="60%">
Eject a cleaner.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_ENABLELIBRARY"></a><a id="ntms_lm_enablelibrary"></a><dl>
<dt><b>NTMS_LM_ENABLELIBRARY</b></dt>
</dl>
</td>
<td width="60%">
Enable the changer.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_ENABLEDRIVE"></a><a id="ntms_lm_enabledrive"></a><dl>
<dt><b>NTMS_LM_ENABLEDRIVE</b></dt>
</dl>
</td>
<td width="60%">
Enable a drive.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_ENABLEMEDIA"></a><a id="ntms_lm_enablemedia"></a><dl>
<dt><b>NTMS_LM_ENABLEMEDIA</b></dt>
</dl>
</td>
<td width="60%">
Enable the medium.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_INJECT"></a><a id="ntms_lm_inject"></a><dl>
<dt><b>NTMS_LM_INJECT</b></dt>
</dl>
</td>
<td width="60%">
Insert the medium into the library.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_INJECTCLEANER"></a><a id="ntms_lm_injectcleaner"></a><dl>
<dt><b>NTMS_LM_INJECTCLEANER</b></dt>
</dl>
</td>
<td width="60%">
Insert a cleaner.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_INVENTORY"></a><a id="ntms_lm_inventory"></a><dl>
<dt><b>NTMS_LM_INVENTORY</b></dt>
</dl>
</td>
<td width="60%">
Perform an inventory of the library.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_MOUNT"></a><a id="ntms_lm_mount"></a><dl>
<dt><b>NTMS_LM_MOUNT</b></dt>
</dl>
</td>
<td width="60%">
Mount a side to a drive.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_PROCESSOMID"></a><a id="ntms_lm_processomid"></a><dl>
<dt><b>NTMS_LM_PROCESSOMID</b></dt>
</dl>
</td>
<td width="60%">
Process the OMID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_RELEASECLEANER"></a><a id="ntms_lm_releasecleaner"></a><dl>
<dt><b>NTMS_LM_RELEASECLEANER</b></dt>
</dl>
</td>
<td width="60%">
Release a cleaner slot.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_REMOVE"></a><a id="ntms_lm_remove"></a><dl>
<dt><b>NTMS_LM_REMOVE</b></dt>
</dl>
</td>
<td width="60%">
Remove a work item from the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_RESERVECLEANER"></a><a id="ntms_lm_reservecleaner"></a><dl>
<dt><b>NTMS_LM_RESERVECLEANER</b></dt>
</dl>
</td>
<td width="60%">
Reserve a cleaner slot.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_UPDATEOMID"></a><a id="ntms_lm_updateomid"></a><dl>
<dt><b>NTMS_LM_UPDATEOMID</b></dt>
</dl>
</td>
<td width="60%">
Update the OMID.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_WRITESCRATCH"></a><a id="ntms_lm_writescratch"></a><dl>
<dt><b>NTMS_LM_WRITESCRATCH</b></dt>
</dl>
</td>
<td width="60%">
Write a free label.

</td>
</tr>
</table>

### -field OperationOption

Work item options (command specific).

### -field State

Current state of this work item. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_QUEUED"></a><a id="ntms_lm_queued"></a><dl>
<dt><b>NTMS_LM_QUEUED</b></dt>
</dl>
</td>
<td width="60%">
Operation is queued.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_INPROCESS"></a><a id="ntms_lm_inprocess"></a><dl>
<dt><b>NTMS_LM_INPROCESS</b></dt>
</dl>
</td>
<td width="60%">
Operation is being processed.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_PASSED"></a><a id="ntms_lm_passed"></a><dl>
<dt><b>NTMS_LM_PASSED</b></dt>
</dl>
</td>
<td width="60%">
Operation completed successfully.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_FAILED"></a><a id="ntms_lm_failed"></a><dl>
<dt><b>NTMS_LM_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Operation has completed with an error.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_WAITING"></a><a id="ntms_lm_waiting"></a><dl>
<dt><b>NTMS_LM_WAITING</b></dt>
</dl>
</td>
<td width="60%">
Operation is blocked.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_CANCELLED"></a><a id="ntms_lm_cancelled"></a><dl>
<dt><b>NTMS_LM_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
Operation has been canceled.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_LM_INVALID"></a><a id="ntms_lm_invalid"></a><dl>
<dt><b>NTMS_LM_INVALID</b></dt>
</dl>
</td>
<td width="60%">
Operation is not valid.

</td>
</tr>
</table>

### -field PartitionId

Unique identifier of a side being serviced.

### -field DriveId

Unique identifier of a drive being serviced.

### -field PhysMediaId

Unique identifier of a piece of physical media being serviced.

### -field Library

Library for this request.

### -field SlotId

Unique identifier of a slot of the piece of physical media being serviced.

### -field TimeQueued

System time that this request was queued to RSM.

### -field TimeCompleted

System time that this request was completed by RSM.

### -field szApplication

Application that submitted the operator request.

### -field szUser

Interactive user logged on to the computer that submitted the operator request.

### -field szComputer

Computer that submitted the operator request.

### -field dwErrorCode

Error return for requests that return with state NTMS_LM_FAILED. This is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

### -field WorkItemId

Associated work item ID for this request. This is currently used to contain the work item ID to be canceled on an NTMS_LM_REMOVE request.

### -field dwPriority

Priority of the work item.

## -remarks

The 
<b>NTMS_LIBREQUESTINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.

GUID in the work times may become not valid over time. For example, an eject of a free medium deletes the PMID after the media is ejected. However the work item is not updated upon completion of the eject.





> [!NOTE]
> The ntmsapi.h header defines NTMS_LIBREQUESTINFORMATION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>
