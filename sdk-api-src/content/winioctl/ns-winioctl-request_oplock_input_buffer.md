---
UID: NS:winioctl._REQUEST_OPLOCK_INPUT_BUFFER
title: REQUEST_OPLOCK_INPUT_BUFFER
description: Contains the information to request an opportunistic lock (oplock) or to acknowledge an oplock break with the FSCTL_REQUEST_OPLOCK control code.
helpviewer_keywords: ["*PREQUEST_OPLOCK_INPUT_BUFFER","OPLOCK_LEVEL_CACHE_HANDLE","OPLOCK_LEVEL_CACHE_READ","OPLOCK_LEVEL_CACHE_WRITE","PREQUEST_OPLOCK_INPUT_BUFFER","PREQUEST_OPLOCK_INPUT_BUFFER structure pointer [Files]","REQUEST_OPLOCK_INPUT_BUFFER","REQUEST_OPLOCK_INPUT_BUFFER structure [Files]","REQUEST_OPLOCK_INPUT_FLAG_ACK","REQUEST_OPLOCK_INPUT_FLAG_REQUEST","fs.request_oplock_input_buffer","winioctl/PREQUEST_OPLOCK_INPUT_BUFFER","winioctl/REQUEST_OPLOCK_INPUT_BUFFER"]
old-location: fs\request_oplock_input_buffer.htm
tech.root: fs
ms.assetid: ac19fbd3-a967-4ac8-9260-93e07b5008ac
ms.date: 12/05/2018
ms.keywords: '*PREQUEST_OPLOCK_INPUT_BUFFER, OPLOCK_LEVEL_CACHE_HANDLE, OPLOCK_LEVEL_CACHE_READ, OPLOCK_LEVEL_CACHE_WRITE, PREQUEST_OPLOCK_INPUT_BUFFER, PREQUEST_OPLOCK_INPUT_BUFFER structure pointer [Files], REQUEST_OPLOCK_INPUT_BUFFER, REQUEST_OPLOCK_INPUT_BUFFER structure [Files], REQUEST_OPLOCK_INPUT_FLAG_ACK, REQUEST_OPLOCK_INPUT_FLAG_REQUEST, fs.request_oplock_input_buffer, winioctl/PREQUEST_OPLOCK_INPUT_BUFFER, winioctl/REQUEST_OPLOCK_INPUT_BUFFER'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: REQUEST_OPLOCK_INPUT_BUFFER, *PREQUEST_OPLOCK_INPUT_BUFFER
req.redist: 
f1_keywords:
 - _REQUEST_OPLOCK_INPUT_BUFFER
 - winioctl/_REQUEST_OPLOCK_INPUT_BUFFER
 - PREQUEST_OPLOCK_INPUT_BUFFER
 - winioctl/PREQUEST_OPLOCK_INPUT_BUFFER
 - REQUEST_OPLOCK_INPUT_BUFFER
 - winioctl/REQUEST_OPLOCK_INPUT_BUFFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - REQUEST_OPLOCK_INPUT_BUFFER
---

# REQUEST_OPLOCK_INPUT_BUFFER structure


## -description

Contains the information to request an opportunistic lock (oplock) or to acknowledge an oplock break 
    with the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock">FSCTL_REQUEST_OPLOCK</a> control 
    code.

## -struct-fields

### -field StructureVersion

The version of the 
      <b>REQUEST_OPLOCK_INPUT_BUFFER</b> structure that 
      is being used. Set this member to <b>REQUEST_OPLOCK_CURRENT_VERSION</b>.

### -field StructureLength

The length of this structure, in bytes. Must be set to 
      <code>sizeof(REQUEST_OPLOCK_INPUT_BUFFER)</code>.

### -field RequestedOplockLevel

A valid combination of the following oplock level values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPLOCK_LEVEL_CACHE_READ"></a><a id="oplock_level_cache_read"></a><dl>
<dt><b>OPLOCK_LEVEL_CACHE_READ</b></dt>
</dl>
</td>
<td width="60%">
Allows clients to cache reads. May be granted to multiple clients.

</td>
</tr>
<tr>
<td width="40%"><a id="OPLOCK_LEVEL_CACHE_HANDLE"></a><a id="oplock_level_cache_handle"></a><dl>
<dt><b>OPLOCK_LEVEL_CACHE_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Allows clients to cache open handles. May be granted to multiple clients.

</td>
</tr>
<tr>
<td width="40%"><a id="OPLOCK_LEVEL_CACHE_WRITE"></a><a id="oplock_level_cache_write"></a><dl>
<dt><b>OPLOCK_LEVEL_CACHE_WRITE</b></dt>
</dl>
</td>
<td width="60%">
Allows clients to cache writes and byte range locks. May be granted only to a single client.

</td>
</tr>
</table>
 

Valid combinations of these values are as follows:

<ul>
<li><code>OPLOCK_LEVEL_CACHE_READ</code></li>
<li><code>OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_HANDLE</code></li>
<li><code>OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_WRITE</code></li>
<li><code>OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_WRITE | OPLOCK_LEVEL_CACHE_HANDLE</code></li>
</ul>
For more information about these value combinations, see 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock">FSCTL_REQUEST_OPLOCK</a>.

### -field Flags

A valid combination of the following request flag values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REQUEST_OPLOCK_INPUT_FLAG_REQUEST"></a><a id="request_oplock_input_flag_request"></a><dl>
<dt><b>REQUEST_OPLOCK_INPUT_FLAG_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Request for a new oplock.  Setting this flag together with 
        <b>REQUEST_OPLOCK_INPUT_FLAG_ACK</b> is not valid and will cause the request to fail with 
        <b>ERROR_INVALID_PARAMETER</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="REQUEST_OPLOCK_INPUT_FLAG_ACK"></a><a id="request_oplock_input_flag_ack"></a><dl>
<dt><b>REQUEST_OPLOCK_INPUT_FLAG_ACK</b></dt>
</dl>
</td>
<td width="60%">
Acknowledgment of an oplock break.  Setting this flag together with 
         <b>REQUEST_OPLOCK_ INPUT_FLAG_REQUEST</b> is not valid and will cause the request to fail 
         with <b>ERROR_INVALID_PARAMETER</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock">FSCTL_REQUEST_OPLOCK</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-request_oplock_output_buffer">REQUEST_OPLOCK_OUTPUT_BUFFER</a>