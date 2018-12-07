---
UID: NS:winioctl._CHANGER_MOVE_MEDIUM
title: "_CHANGER_MOVE_MEDIUM"
author: windows-sdk-content
description: Contains information that the IOCTL_CHANGER_MOVE_MEDIUM control code uses to move a piece of media to a destination.
old-location: base\changer_move_medium_str.htm
tech.root: devio
ms.assetid: 9a837686-c081-4365-9560-be64c5d343cb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCHANGER_MOVE_MEDIUM, CHANGER_MOVE_MEDIUM, CHANGER_MOVE_MEDIUM structure, PCHANGER_MOVE_MEDIUM, PCHANGER_MOVE_MEDIUM structure pointer, _CHANGER_MOVE_MEDIUM, _win32_changer_move_medium_str, base.changer_move_medium_str, winioctl/CHANGER_MOVE_MEDIUM, winioctl/PCHANGER_MOVE_MEDIUM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CHANGER_MOVE_MEDIUM
product: Windows
targetos: Windows
req.typenames: CHANGER_MOVE_MEDIUM, *PCHANGER_MOVE_MEDIUM
req.redist: 
---

# _CHANGER_MOVE_MEDIUM structure


## -description


Contains information that the 
<a href="https://msdn.microsoft.com/73fa826c-ef7f-4341-838e-73e025d8d1c1">IOCTL_CHANGER_MOVE_MEDIUM</a> control code uses to move a piece of media to a destination.


## -struct-fields




### -field Transport

A 
<a href="https://msdn.microsoft.com/96e9803b-16c4-415c-940a-f5df3edff3b3">CHANGER_ELEMENT</a> structure that indicates which transport element to use for the move operation.


### -field Source

A 
<a href="https://msdn.microsoft.com/96e9803b-16c4-415c-940a-f5df3edff3b3">CHANGER_ELEMENT</a> structure that indicates the element that contains the media that is to be moved.


### -field Destination

A 
<a href="https://msdn.microsoft.com/96e9803b-16c4-415c-940a-f5df3edff3b3">CHANGER_ELEMENT</a> structure that indicates the element that is the destination of the media originally at <b>Source</b>.


### -field Flip

If this member is <b>TRUE</b>, the media should be flipped. Otherwise, it should not. This member is valid only if the <b>Features0</b> member of the 
<a href="https://msdn.microsoft.com/ad5b6cc3-19f1-4196-9f03-791f342d0cf9">GET_CHANGER_PARAMETERS</a> structure is CHANGER_MEDIUM_FLIP.


## -see-also




<a href="https://msdn.microsoft.com/96e9803b-16c4-415c-940a-f5df3edff3b3">CHANGER_ELEMENT</a>



<a href="https://msdn.microsoft.com/73fa826c-ef7f-4341-838e-73e025d8d1c1">IOCTL_CHANGER_MOVE_MEDIUM</a>
 

 

