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

# _DEV_BROADCAST_VOLUME structure


## -description


Contains information about a logical volume.


## -struct-fields




### -field dbcv_size

The size of this structure, in bytes.


### -field dbcv_devicetype

Set to <b>DBT_DEVTYP_VOLUME</b> (2).


### -field dbcv_reserved

Reserved; do not use.


### -field dbcv_unitmask

The logical unit mask identifying one or more logical units. Each bit in the mask corresponds to one 
      logical drive. Bit 0 represents drive A, bit 1 represents drive B, and so on.


### -field dbcv_flags

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DBTF_MEDIA"></a><a id="dbtf_media"></a><dl>
<dt><b>DBTF_MEDIA</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Change affects media in drive. If not set, change affects physical device or drive.

</td>
</tr>
<tr>
<td width="40%"><a id="DBTF_NET"></a><a id="dbtf_net"></a><dl>
<dt><b>DBTF_NET</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Indicated logical volume is a network volume.

</td>
</tr>
</table>
 


## -remarks



Although the <b>dbcv_unitmask</b> member may specify more than one volume in any message, 
    this does not guarantee that only one message is generated for a specified event. Multiple system features may 
    independently generate messages for logical volumes at the same time.

Messages for media arrival and removal are sent only for media in devices that support a soft-eject mechanism. 
    For example, applications will not see media-related volume messages for floppy disks.

Messages for network drive arrival and removal are not sent whenever network commands are issued, but rather 
    when network connections will disappear as the result of a hardware event.




## -see-also




<a href="https://msdn.microsoft.com/4fc81fcb-b9fe-4016-b639-a43845af2c5f">DEV_BROADCAST_HDR</a>



<a href="https://msdn.microsoft.com/b64a3983-ee75-4199-9778-1e5b7cec59e4">WM_DEVICECHANGE</a>
 

 

