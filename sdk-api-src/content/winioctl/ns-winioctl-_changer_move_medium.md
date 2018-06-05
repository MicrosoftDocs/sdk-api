---
UID: NS:winioctl._CHANGER_MOVE_MEDIUM
title: "_CHANGER_MOVE_MEDIUM"
author: windows-sdk-content
description: Contains information that the IOCTL_CHANGER_MOVE_MEDIUM control code uses to move a piece of media to a destination.
old-location: base\changer_move_medium_str.htm
old-project: DevIO
ms.assetid: 9a837686-c081-4365-9560-be64c5d343cb
ms.author: windowssdkdev
ms.date: 04/03/2018
ms.keywords: "*PCHANGER_MOVE_MEDIUM, CHANGER_MOVE_MEDIUM, CHANGER_MOVE_MEDIUM structure, PCHANGER_MOVE_MEDIUM, PCHANGER_MOVE_MEDIUM structure pointer, _CHANGER_MOVE_MEDIUM, _win32_changer_move_medium_str, base.changer_move_medium_str, winioctl/CHANGER_MOVE_MEDIUM, winioctl/PCHANGER_MOVE_MEDIUM"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CHANGER_MOVE_MEDIUM, *PCHANGER_MOVE_MEDIUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	CHANGER_MOVE_MEDIUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CHANGER_MOVE_MEDIUM structure


## -description


Contains information that the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559410">IOCTL_CHANGER_MOVE_MEDIUM</a> control code uses to move a piece of media to a destination.


## -struct-fields




### -field Transport

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551457">CHANGER_ELEMENT</a> structure that indicates which transport element to use for the move operation.


### -field Source

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551457">CHANGER_ELEMENT</a> structure that indicates the element that contains the media that is to be moved.


### -field Destination

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551457">CHANGER_ELEMENT</a> structure that indicates the element that is the destination of the media originally at <b>Source</b>.


### -field Flip

If this member is <b>TRUE</b>, the media should be flipped. Otherwise, it should not. This member is valid only if the <b>Features0</b> member of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff554979">GET_CHANGER_PARAMETERS</a> structure is CHANGER_MEDIUM_FLIP.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551457">CHANGER_ELEMENT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559410">IOCTL_CHANGER_MOVE_MEDIUM</a>
 

 

