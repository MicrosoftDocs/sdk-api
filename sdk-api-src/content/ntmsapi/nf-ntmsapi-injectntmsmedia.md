---
UID: NF:ntmsapi.InjectNtmsMedia
title: InjectNtmsMedia function (ntmsapi.h)
description: The InjectNtmsMedia function allows media to be inserted into the port of the specified library. If the library is busy, RSM queues InjectNtmsMedia and returns success.
helpviewer_keywords: ["InjectNtmsMedia","InjectNtmsMedia function [Files]","NTMS_INJECT_RETRACT","NTMS_INJECT_START","NTMS_INJECT_START_MANY","NTMS_INJECT_STOP","_zaw_injectntmsmedia","base.injectntmsmedia","fs.injectntmsmedia","ntmsapi/InjectNtmsMedia"]
old-location: fs\injectntmsmedia.htm
tech.root: fs
ms.assetid: c4274c9c-f052-42dd-859b-85606d455001
ms.date: 12/05/2018
ms.keywords: InjectNtmsMedia, InjectNtmsMedia function [Files], NTMS_INJECT_RETRACT, NTMS_INJECT_START, NTMS_INJECT_START_MANY, NTMS_INJECT_STOP, _zaw_injectntmsmedia, base.injectntmsmedia, fs.injectntmsmedia, ntmsapi/InjectNtmsMedia
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
 - InjectNtmsMedia
 - ntmsapi/InjectNtmsMedia
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
 - InjectNtmsMedia
---

# InjectNtmsMedia function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>InjectNtmsMedia</b> function allows media to be inserted into the port of the specified library. If the library is busy, RSM queues 
<b>InjectNtmsMedia</b> and returns success.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpLibraryId [in]

Unique identifier of a library object.

### -param lpInjectOperation [out]

GUID of the insert library operation. If <i>dwAction</i> is NTMS_INJECT_START, this parameter receives the GUID for the operation. If <i>dwAction</i> is NTMS_INJECT_STOP, this parameter must be set to the GUID for the operation to be stopped.

### -param dwAction [in]

This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_INJECT_START"></a><a id="ntms_inject_start"></a><dl>
<dt><b>NTMS_INJECT_START</b></dt>
</dl>
</td>
<td width="60%">
Start the insert operation with a port. Media is repeatedly inserted until the time-out event occurs or the function is called again with NTMS_INJECT_STOP.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_INJECT_STOP"></a><a id="ntms_inject_stop"></a><dl>
<dt><b>NTMS_INJECT_STOP</b></dt>
</dl>
</td>
<td width="60%">
Terminate the insertion process prior to the time-out event lapsing.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_INJECT_RETRACT"></a><a id="ntms_inject_retract"></a><dl>
<dt><b>NTMS_INJECT_RETRACT</b></dt>
</dl>
</td>
<td width="60%">
Direct the library to retract the insert/eject port and check for media placed there by the operator.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_INJECT_START_MANY"></a><a id="ntms_inject_start_many"></a><dl>
<dt><b>NTMS_INJECT_START_MANY</b></dt>
</dl>
</td>
<td width="60%">
Direct the insert/eject port to open continually and check for media placed there by the operator. If a medium is found, the insert/eject port is reopened to receive more media.

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
NTMS_CONTROL_ACCESS to the library is denied. Other security errors are also possible, but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database is inaccessible or damaged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FULL</b></dt>
</dl>
</td>
<td width="60%">
The database is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The library is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session ID is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
A Stop action  was performed on an operation ID that was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The library ID or operation ID pointer is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_LIBRARY_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The library ID refers to an offline library that cannot eject media.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was an allocation failure during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The insert is queued.

</td>
</tr>
</table>

## -remarks

This function returns to the application as soon as the insert request is queued.

If the library specified by the 
<b>InjectNtmsMedia</b> function does not have a port, use the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-accessntmslibrarydoor">AccessNtmsLibraryDoor</a> function to insert and eject media.

This function cannot be used with the offline library.

Insert begins the process of inserting media into a library. Because libraries vary on the functionality of the NTMS_IEPORT object, each device may operate slightly differently. The following steps describe how RSM generally handles an inject:

<p class="proch"><b>To insert media into a library</b>

<ol>
<li>Allow/unlock/extend the NTMS_IEPORT.</li>
<li>Poll for a full NTMS_IEPORT, a retracted NTMS_IEPORT, a Stop Inject command, or a time-out value. If none of these have occurred, continue to wait. (Multi-cartridge insert/eject ports are not scanned for full status.)</li>
<li>When one of the preceding events occurs, the NTMS_IEPORT is locked, each medium in the NTMS_IEPORT is moved to a slot, and an identify medium command is queued for each medium.</li>
</ol>
If there are not enough slots for the media in the NTMS_IEPORT object, the media remains in the NTMS_IEPORT object and an Operator Request is posted to have media removed from the library.

If there are no free slots, the 
<b>InjectNtmsMedia</b> function receives an error.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-ejectntmsmedia">EjectNtmsMedia</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>