---
UID: NE:winioctl._ELEMENT_TYPE
title: ELEMENT_TYPE
description: Specifies the element type of a changer device.
helpviewer_keywords: ["*PELEMENT_TYPE","AllElements","ChangerDoor","ChangerDrive","ChangerIEPort","ChangerKeypad","ChangerSlot","ChangerTransport","ELEMENT_TYPE","ELEMENT_TYPE enumeration","PELEMENT_TYPE","PELEMENT_TYPE enumeration pointer","_win32_element_type_str","base.element_type_str","winioctl/AllElements","winioctl/ChangerDoor","winioctl/ChangerDrive","winioctl/ChangerIEPort","winioctl/ChangerKeypad","winioctl/ChangerSlot","winioctl/ChangerTransport","winioctl/ELEMENT_TYPE","winioctl/PELEMENT_TYPE"]
old-location: base\element_type_str.htm
tech.root: base
ms.assetid: b026d0f5-133d-4138-a727-80bf4480bb74
ms.date: 12/05/2018
ms.keywords: '*PELEMENT_TYPE, AllElements, ChangerDoor, ChangerDrive, ChangerIEPort, ChangerKeypad, ChangerSlot, ChangerTransport, ELEMENT_TYPE, ELEMENT_TYPE enumeration, PELEMENT_TYPE, PELEMENT_TYPE enumeration pointer, _win32_element_type_str, base.element_type_str, winioctl/AllElements, winioctl/ChangerDoor, winioctl/ChangerDrive, winioctl/ChangerIEPort, winioctl/ChangerKeypad, winioctl/ChangerSlot, winioctl/ChangerTransport, winioctl/ELEMENT_TYPE, winioctl/PELEMENT_TYPE'
req.header: winioctl.h
req.include-header: Windows.h
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
req.typenames: ELEMENT_TYPE, *PELEMENT_TYPE
req.redist: 
f1_keywords:
 - _ELEMENT_TYPE
 - winioctl/_ELEMENT_TYPE
 - PELEMENT_TYPE
 - winioctl/PELEMENT_TYPE
 - ELEMENT_TYPE
 - winioctl/ELEMENT_TYPE
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
 - ELEMENT_TYPE
---

# ELEMENT_TYPE enumeration


## -description

Specifies the element type of a changer device.

## -enum-fields

### -field AllElements

All elements of a changer, including its robotic transport, drives, slots, and insert/eject ports. This value is valid only with 
[IOCTL_CHANGER_GET_ELEMENT_STATUS](ni-winioctl-ioctl_changer_get_element_status.md) or [IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS](ni-winioctl-ioctl_changer_initialize_element_status.md).

### -field ChangerTransport

Robotic transport element, which is used to move media between insert/eject ports, slots, and drives.

### -field ChangerSlot

Storage element, which is a slot in the changer in which media is stored when not mounted in a drive.

### -field ChangerIEPort

Insert/eject port, which is a single- or multiple-cartridge access port in some changers. An element is an insert/eject port only if it is possible to move a piece of media from a slot to the insert/eject port.

### -field ChangerDrive

Data transfer element where data can be read from and written to media.

### -field ChangerDoor

Mechanism that provides access to all media in a changer at one time (as compared to an IEport that provides access to one or more, but not all, media). For example, a large front door or a magazine that contains all media in the changer is an element of this type. This value is valid only with [IOCTL_CHANGER_SET_ACCESS](ni-winioctl-ioctl_changer_set_access.md).

### -field ChangerKeypad

Keypad or other input control on the front panel of a changer. This value is valid only with [IOCTL_CHANGER_SET_ACCESS](ni-winioctl-ioctl_changer_set_access.md).

### -field ChangerMaxElement

## -see-also

* [CHANGER_ELEMENT](ns-winioctl-changer_element.md)

