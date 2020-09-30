---
UID: NS:dbt._DEV_BROADCAST_HDR
title: DEV_BROADCAST_HDR (dbt.h)
description: Serves as a standard header for information related to a device event reported through the WM_DEVICECHANGE message.
helpviewer_keywords: ["DBT_DEVTYP_DEVICEINTERFACE","DBT_DEVTYP_HANDLE","DBT_DEVTYP_OEM","DBT_DEVTYP_PORT","DBT_DEVTYP_VOLUME","DEV_BROADCAST_HDR","DEV_BROADCAST_HDR structure","PDEV_BROADCAST_HDR","PDEV_BROADCAST_HDR structure pointer","_win32_dev_broadcast_hdr_str","base.dev_broadcast_hdr_str","dbt/DEV_BROADCAST_HDR","dbt/PDEV_BROADCAST_HDR"]
old-location: base\dev_broadcast_hdr_str.htm
tech.root: base
ms.assetid: 4fc81fcb-b9fe-4016-b639-a43845af2c5f
ms.date: 12/05/2018
ms.keywords: DBT_DEVTYP_DEVICEINTERFACE, DBT_DEVTYP_HANDLE, DBT_DEVTYP_OEM, DBT_DEVTYP_PORT, DBT_DEVTYP_VOLUME, DEV_BROADCAST_HDR, DEV_BROADCAST_HDR structure, PDEV_BROADCAST_HDR, PDEV_BROADCAST_HDR structure pointer, _win32_dev_broadcast_hdr_str, base.dev_broadcast_hdr_str, dbt/DEV_BROADCAST_HDR, dbt/PDEV_BROADCAST_HDR
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
req.typenames: DEV_BROADCAST_HDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DEV_BROADCAST_HDR
 - dbt/_DEV_BROADCAST_HDR
 - DEV_BROADCAST_HDR
 - dbt/DEV_BROADCAST_HDR
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
 - DEV_BROADCAST_HDR
---

# DEV_BROADCAST_HDR structure


## -description

Serves as a standard header for information related to a device event reported through the 
<a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a> message.

The members of the 
<b>DEV_BROADCAST_HDR</b> structure are contained in each device management structure. To determine which structure you have received through 
<a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>, treat the structure as a 
<b>DEV_BROADCAST_HDR</b> structure and check its <b>dbch_devicetype</b> member.

## -struct-fields

### -field dbch_size

The size of this structure, in bytes. 




If this is a user-defined event, this member must be the size of this header, plus the size of the variable-length data in the 
<a href="/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined">_DEV_BROADCAST_USERDEFINED</a> structure.

### -field dbch_devicetype

The device type, which determines the event-specific information that follows the first three members. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DBT_DEVTYP_DEVICEINTERFACE"></a><a id="dbt_devtyp_deviceinterface"></a><dl>
<dt><b>DBT_DEVTYP_DEVICEINTERFACE</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Class of devices. This structure is a 
<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a">DEV_BROADCAST_DEVICEINTERFACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="DBT_DEVTYP_HANDLE"></a><a id="dbt_devtyp_handle"></a><dl>
<dt><b>DBT_DEVTYP_HANDLE</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
File system handle. This structure is a 
<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle">DEV_BROADCAST_HANDLE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="DBT_DEVTYP_OEM"></a><a id="dbt_devtyp_oem"></a><dl>
<dt><b>DBT_DEVTYP_OEM</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
OEM- or IHV-defined device type. This structure is a 
<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_oem">DEV_BROADCAST_OEM</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="DBT_DEVTYP_PORT"></a><a id="dbt_devtyp_port"></a><dl>
<dt><b>DBT_DEVTYP_PORT</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Port device (serial or parallel). This structure is a 
<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_port_a">DEV_BROADCAST_PORT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="DBT_DEVTYP_VOLUME"></a><a id="dbt_devtyp_volume"></a><dl>
<dt><b>DBT_DEVTYP_VOLUME</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Logical volume. This structure is a 
<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_volume">DEV_BROADCAST_VOLUME</a> structure.

</td>
</tr>
</table>

### -field dbch_reserved

Reserved; do not use.

## -see-also

<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a">DEV_BROADCAST_DEVICEINTERFACE</a>



<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle">DEV_BROADCAST_HANDLE</a>



<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_oem">DEV_BROADCAST_OEM</a>



<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_port_a">DEV_BROADCAST_PORT</a>



<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_volume">DEV_BROADCAST_VOLUME</a>



<a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>