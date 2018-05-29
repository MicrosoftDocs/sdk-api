---
UID: NS:ntddmou._MOUSE_UNIT_ID_PARAMETER
title: "_MOUSE_UNIT_ID_PARAMETER"
author: windows-sdk-content
description: MOUSE_UNIT_ID_PARAMETER specifies a unit ID that Mouclass assigns to a mouse.
old-location: hid\mouse_unit_id_parameter.htm
old-project: hid
ms.assetid: c121e9af-29c3-4638-9c21-2dc45c572858
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: "*PMOUSE_UNIT_ID_PARAMETER, MOUSE_UNIT_ID_PARAMETER, MOUSE_UNIT_ID_PARAMETER structure [Human Input Devices], PMOUSE_UNIT_ID_PARAMETER, PMOUSE_UNIT_ID_PARAMETER structure pointer [Human Input Devices], _MOUSE_UNIT_ID_PARAMETER, hid.mouse_unit_id_parameter, mref_596482c8-d90d-4505-9b30-567bd8468691.xml, ntddmou/MOUSE_UNIT_ID_PARAMETER, ntddmou/PMOUSE_UNIT_ID_PARAMETER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: MOUSE_UNIT_ID_PARAMETER, *PMOUSE_UNIT_ID_PARAMETER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddmou.h
api_name:
-	MOUSE_UNIT_ID_PARAMETER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _MOUSE_UNIT_ID_PARAMETER structure


## -description


MOUSE_UNIT_ID_PARAMETER specifies a unit ID that Mouclass assigns to a mouse.


## -struct-fields




### -field UnitId

Specifies the unit number of the mouse device. A mouse <a href="https://msdn.microsoft.com/dfcc7338-7c4d-4b4c-9a13-c76bfe82f5a9">device name</a> has the format \Device\PointerPort<i>N</i>, where the suffix <i>N </i>is the unit number of the device. For example, a device, whose name is \Device\PointerPort0, has a unit number of zero, and a device, whose name is \Device\PointerPort1, has a unit number of one.


## -remarks



Although this structure is used with an <a href="https://msdn.microsoft.com/library/windows/hardware/ff542080">IOCTL_MOUSE_QUERY_ATTRIBUTES</a> request, Mouclass does not use the <b>UnitId</b> value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff542080">IOCTL_MOUSE_QUERY_ATTRIBUTES</a>
 

 

