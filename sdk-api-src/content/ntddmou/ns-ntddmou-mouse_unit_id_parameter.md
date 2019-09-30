---
UID: NS:ntddmou._MOUSE_UNIT_ID_PARAMETER
title: MOUSE_UNIT_ID_PARAMETER (ntddmou.h)
author: windows-sdk-content
description: MOUSE_UNIT_ID_PARAMETER specifies a unit ID that Mouclass assigns to a mouse.
old-location: hid\mouse_unit_id_parameter.htm
tech.root: hid
ms.assetid: c121e9af-29c3-4638-9c21-2dc45c572858
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMOUSE_UNIT_ID_PARAMETER, MOUSE_UNIT_ID_PARAMETER, MOUSE_UNIT_ID_PARAMETER structure [Human Input Devices], PMOUSE_UNIT_ID_PARAMETER, PMOUSE_UNIT_ID_PARAMETER structure pointer [Human Input Devices], hid.mouse_unit_id_parameter, mref_596482c8-d90d-4505-9b30-567bd8468691.xml, ntddmou/MOUSE_UNIT_ID_PARAMETER, ntddmou/PMOUSE_UNIT_ID_PARAMETER"
ms.topic: struct
f1_keywords: 
 - "ntddmou/MOUSE_UNIT_ID_PARAMETER"
req.header: ntddmou.h
req.include-header: Ntddmou.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddmou.h
api_name:
 - MOUSE_UNIT_ID_PARAMETER
targetos: Windows
req.typenames: MOUSE_UNIT_ID_PARAMETER, *PMOUSE_UNIT_ID_PARAMETER
req.redist: 
ms.custom: 19H1
---

# MOUSE_UNIT_ID_PARAMETER structure


## -description


MOUSE_UNIT_ID_PARAMETER specifies a unit ID that Mouclass assigns to a mouse.


## -struct-fields




### -field UnitId

Specifies the unit number of the mouse device. A mouse <a href="https://docs.microsoft.com/windows-hardware/drivers/kernel/nt-device-names">device name</a> has the format \Device\PointerPort<i>N</i>, where the suffix <i>N </i>is the unit number of the device. For example, a device, whose name is \Device\PointerPort0, has a unit number of zero, and a device, whose name is \Device\PointerPort1, has a unit number of one.


## -remarks



Although this structure is used with an <a href="https://docs.microsoft.com/windows/desktop/api/ntddmou/ni-ntddmou-ioctl_mouse_query_attributes">IOCTL_MOUSE_QUERY_ATTRIBUTES</a> request, Mouclass does not use the <b>UnitId</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntddmou/ni-ntddmou-ioctl_mouse_query_attributes">IOCTL_MOUSE_QUERY_ATTRIBUTES</a>
 

 

