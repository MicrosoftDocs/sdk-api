---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _REQUEST_OPLOCK_OUTPUT_BUFFER structure


## -description


Contains the opportunistic lock (oplock) information returned by the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff545530">FSCTL_REQUEST_OPLOCK</a> control code.


## -struct-fields




### -field StructureVersion

The version of the 
      <b>REQUEST_OPLOCK_OUTPUT_BUFFER</b> structure that 
      is being used.


### -field StructureLength

The length of this structure, in bytes. 


### -field OriginalOplockLevel

One or more <b>OPLOCK_LEVEL_CACHE_</b><i>XXX</i> values that indicate 
       the level of the oplock that was broken.

For possible values, see the <b>RequestedOplockLevel</b> member of the 
       <a href="https://msdn.microsoft.com/ac19fbd3-a967-4ac8-9260-93e07b5008ac">REQUEST_OPLOCK_INPUT_BUFFER</a> structure.


### -field NewOplockLevel

One or more <b>OPLOCK_LEVEL_CACHE_</b><i>XXX</i> values that indicate 
       the level to which an oplock is being broken, or an oplock level that may be available for granting, depending 
       on the operation returning this buffer.

For possible values, see the <b>RequestedOplockLevel</b> member of the 
       <a href="https://msdn.microsoft.com/ac19fbd3-a967-4ac8-9260-93e07b5008ac">REQUEST_OPLOCK_INPUT_BUFFER</a> structure.


### -field Flags

One or more <b>REQUEST_OPLOCK_OUTPUT_FLAG_</b><i>XXX</i> values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REQUEST_OPLOCK_OUTPUT_FLAG_ACK_REQUIRED"></a><a id="request_oplock_output_flag_ack_required"></a><dl>
<dt><b>REQUEST_OPLOCK_OUTPUT_FLAG_ACK_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that an acknowledgment is required, and the oplock described in 
        <b>OriginalOplockLevel</b> will continue to remain in force until the break is 
        successfully acknowledged.

</td>
</tr>
<tr>
<td width="40%"><a id="REQUEST_OPLOCK_OUTPUT_FLAG_MODES_PROVIDED"></a><a id="request_oplock_output_flag_modes_provided"></a><dl>
<dt><b>REQUEST_OPLOCK_OUTPUT_FLAG_MODES_PROVIDED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>ShareMode</b> and <b>AccessMode</b> members 
        contain the share and access flags, respectively, of the request causing the oplock break. For more 
        information, see the Remarks section.

</td>
</tr>
</table>
 


### -field AccessMode

If the <b>REQUEST_OPLOCK_OUTPUT_FLAG_MODES_PROVIDED</b> flag is set and the 
      <b>OPLOCK_LEVEL_CACHE_HANDLE</b> level is being lost in an oplock break, contains the access 
      mode mode of the request that is causing the break.


### -field ShareMode

If the <b>REQUEST_OPLOCK_OUTPUT_FLAG_MODES_PROVIDED</b> flag is set and the 
      <b>OPLOCK_LEVEL_CACHE_HANDLE</b> level is being lost in an oplock break, contains the share 
      mode of the request that is causing the break.


## -remarks



The <b>REQUEST_OPLOCK_OUTPUT_FLAG_MODES_PROVIDED</b> flag indicates that the 
    <b>ShareMode</b> and <b>AccessMode</b> fields contain the share and access 
    flags, respectively, of the request causing the oplock break. This information may be provided on breaks where the 
    <b>OPLOCK_LEVEL_CACHE_HANDLE</b> level is being lost and may be useful to callers who can close 
    handles whose share and access modes conflict with the handle causing the break. This may enable them to maintain 
    at least some handle cache state. Note that not all breaks where the 
    <b>OPLOCK_LEVEL_CACHE_HANDLE</b> level is being lost will have this flag set. The primary case 
    where this flag will be set is if the break is a result of a create operation that needs the 
    <b>OPLOCK_LEVEL_CACHE_HANDLE</b> oplock to be broken to avoid failing with 
    <b>ERROR_SHARING_VIOLATION</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545530">FSCTL_REQUEST_OPLOCK</a>



<a href="ifsk.oplock_semantics">Oplock Semantics</a>



<a href="https://msdn.microsoft.com/ac19fbd3-a967-4ac8-9260-93e07b5008ac">REQUEST_OPLOCK_INPUT_BUFFER</a>
 

 

