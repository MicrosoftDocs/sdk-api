---
UID: NF:winuser.GID_ROTATE_ANGLE_TO_ARGUMENT
title: GID_ROTATE_ANGLE_TO_ARGUMENT macro
author: windows-sdk-content
description: Converts a radian value to an argument for rotation gesture messages.
old-location: wintouch\gci_rotate_angle_to_argument.htm
tech.root: wintouch
ms.assetid: 058c914e-82c7-40f9-8d0d-2a6a8e77cee0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GID_ROTATE_ANGLE_TO_ARGUMENT, GID_ROTATE_ANGLE_TO_ARGUMENT macro [Windows Touch], wintouch.gci_rotate_angle_to_argument, winuser/GID_ROTATE_ANGLE_TO_ARGUMENT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - winuser.h
api_name:
 - GID_ROTATE_ANGLE_TO_ARGUMENT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- winuser.h
: 
- GID_ROTATE_ANGLE_TO_ARGUMENT
: 
---

# GID_ROTATE_ANGLE_TO_ARGUMENT macro


## -description


Converts a radian value to an argument for rotation gesture messages.


## -parameters




### -param _arg_

The angle of rotation as a double in radians.


## -remarks



<div class="alert"><b>Note</b>  The macro assumes that the input value for the radian value is between -2*pi and 2*pi.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/00877809-e8c7-41a5-928b-2cf66364d42a">Macros</a>
 

 

