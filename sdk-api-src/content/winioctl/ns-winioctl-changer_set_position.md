---
UID: NS:winioctl._CHANGER_SET_POSITION
title: CHANGER_SET_POSITION
description: Contains information needed by the IOCTL_CHANGER_SET_POSITION control code to set the changer's robotic transport mechanism to the specified element address.
helpviewer_keywords: ["*PCHANGER_SET_POSITION","CHANGER_SET_POSITION","CHANGER_SET_POSITION structure","PCHANGER_SET_POSITION","PCHANGER_SET_POSITION structure pointer","_win32_changer_set_position_str","base.changer_set_position_str","winioctl/CHANGER_SET_POSITION","winioctl/PCHANGER_SET_POSITION"]
old-location: base\changer_set_position_str.htm
tech.root: base
ms.assetid: 7bffff12-666d-4203-bddd-32f279d18fb4
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_SET_POSITION, CHANGER_SET_POSITION, CHANGER_SET_POSITION structure, PCHANGER_SET_POSITION, PCHANGER_SET_POSITION structure pointer, _win32_changer_set_position_str, base.changer_set_position_str, winioctl/CHANGER_SET_POSITION, winioctl/PCHANGER_SET_POSITION'
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
req.typenames: CHANGER_SET_POSITION, *PCHANGER_SET_POSITION
req.redist: 
f1_keywords:
 - _CHANGER_SET_POSITION
 - winioctl/_CHANGER_SET_POSITION
 - PCHANGER_SET_POSITION
 - winioctl/PCHANGER_SET_POSITION
 - CHANGER_SET_POSITION
 - winioctl/CHANGER_SET_POSITION
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
 - CHANGER_SET_POSITION
---

# CHANGER_SET_POSITION structure


## -description

Contains information needed by the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_set_position">IOCTL_CHANGER_SET_POSITION</a> control code to set the changer's robotic transport mechanism to the specified element address.

## -struct-fields

### -field Transport

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that indicates the transport to be moved. The <b>ElementType</b> member must be ChangerTransport.

### -field Destination

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that indicates the final destination of the transport. The <b>ElementType</b> member must be one of the following values: ChangerSlot, ChangerDrive, or ChangerIEPort.

### -field Flip

If this member is <b>TRUE</b>, the media currently carried by <b>Transport</b> should be flipped. Otherwise, it should not. This member is valid only if the <b>Features0</b> member of the 
<a href="/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a> structure is CHANGER_MEDIUM_FLIP.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_set_position">IOCTL_CHANGER_SET_POSITION</a>