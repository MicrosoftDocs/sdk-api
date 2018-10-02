---
UID: NF:winuser.GetPointerDeviceRects
title: GetPointerDeviceRects function
author: windows-sdk-content
description: Gets the x and y range for the pointer device (in himetric) and the x and y range (current resolution) for the display that the pointer device is mapped to.
old-location: input_pointerdevice\getpointerdevicerects.htm
tech.root: Input_PointerDevice
ms.assetid: a6586dec-6d57-4345-be56-89c7308c1097
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPointerDeviceRects, GetPointerDeviceRects function, input_pointerdevice.getpointerdevicerects, unifiedinputstack.getpointerdevicerects, winuser/GetPointerDeviceRects
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
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - GetPointerDeviceRects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPointerDeviceRects function


## -description


Gets the x and y range for the pointer device (in himetric) and the x and y range (current resolution) for the display that the pointer device is mapped to. 


## -parameters




### -param device [in]

The handle to the pointer device.


### -param pointerDeviceRect [out]

The structure for retrieving the device's physical range data.


### -param displayRect [out]

The structure for retrieving the display resolution.


## -returns



TRUE if the function succeeds; otherwise, FALSE. If the function fails, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for more information.




## -see-also




<a href="https://msdn.microsoft.com/44942954-3EA6-4C33-8CF1-E8BF72A914CB">Functions</a>
 

 

