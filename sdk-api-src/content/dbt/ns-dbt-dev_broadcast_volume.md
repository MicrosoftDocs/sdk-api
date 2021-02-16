---
UID: NS:dbt._DEV_BROADCAST_VOLUME
title: DEV_BROADCAST_VOLUME (dbt.h)
description: Contains information about a logical volume.
helpviewer_keywords: ["DBTF_MEDIA","DBTF_NET","DEV_BROADCAST_VOLUME","DEV_BROADCAST_VOLUME structure","PDEV_BROADCAST_VOLUME","PDEV_BROADCAST_VOLUME structure pointer","_win32_dev_broadcast_volume_str","base.dev_broadcast_volume_str","dbt/DEV_BROADCAST_VOLUME","dbt/PDEV_BROADCAST_VOLUME"]
old-location: base\dev_broadcast_volume_str.htm
tech.root: base
ms.assetid: 8ce644d9-1e95-458e-924f-67bd37831048
ms.date: 12/05/2018
ms.keywords: DBTF_MEDIA, DBTF_NET, DEV_BROADCAST_VOLUME, DEV_BROADCAST_VOLUME structure, PDEV_BROADCAST_VOLUME, PDEV_BROADCAST_VOLUME structure pointer, _win32_dev_broadcast_volume_str, base.dev_broadcast_volume_str, dbt/DEV_BROADCAST_VOLUME, dbt/PDEV_BROADCAST_VOLUME
req.header: dbt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: DEV_BROADCAST_VOLUME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DEV_BROADCAST_VOLUME
 - dbt/_DEV_BROADCAST_VOLUME
 - DEV_BROADCAST_VOLUME
 - dbt/DEV_BROADCAST_VOLUME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dbt.h
api_name:
 - DEV_BROADCAST_VOLUME
---

# DEV_BROADCAST_VOLUME structure


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

<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_hdr">DEV_BROADCAST_HDR</a>



<a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>