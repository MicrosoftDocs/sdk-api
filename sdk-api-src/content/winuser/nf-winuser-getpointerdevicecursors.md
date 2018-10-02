---
UID: NF:winuser.GetPointerDeviceCursors
title: GetPointerDeviceCursors function
author: windows-sdk-content
description: Gets the cursor IDs that are mapped to the cursors associated with a pointer device.
old-location: input_pointerdevice\getpointerdevicecursors.htm
tech.root: Input_PointerDevice
ms.assetid: 4dd25033-e63a-4fa9-89b9-bfcae4061a76
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPointerDeviceCursors, GetPointerDeviceCursors function, input_pointerdevice.getpointerdevicecursors, unifiedinputstack.getpointerdevicecursors, winuser/GetPointerDeviceCursors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetPointerDeviceCursors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPointerDeviceCursors function


## -description


Gets the cursor IDs that are mapped to the cursors associated with a pointer device.


## -parameters




### -param device [in]

The device handle.


### -param cursorCount [in, out]

The number of cursors associated with the pointer device. 


### -param deviceCursors [out, optional]

An array of <a href="https://msdn.microsoft.com/5d71e5b4-95eb-453e-9164-e7659ef4059e">POINTER_DEVICE_CURSOR_INFO</a> structures that contain info about the cursors. If NULL, <i>cursorCount</i> returns the number of cursors associated with the pointer device.


## -returns



TRUE if the function succeeds; otherwise, FALSE. If the function fails, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for more information.






## -see-also




<a href="https://msdn.microsoft.com/44942954-3EA6-4C33-8CF1-E8BF72A914CB">Functions</a>
 

 

