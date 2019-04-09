---
UID: NF:winuser.GetPointerDevice
title: GetPointerDevice function (winuser.h)
author: windows-sdk-content
description: Gets information about the pointer device.
old-location: input_pointerdevice\getpointerdevice.htm
tech.root: Input_PointerDevice
ms.assetid: 800E0BFE-6E57-4EAA-B47C-FEEC0B5BFA2F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPointerDevice, GetPointerDevice function, input_pointerdevice.getpointerdevice, unifiedinputstack.getpointerdevice, winuser/GetPointerDevice
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
 - GetPointerDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPointerDevice function


## -description


Gets information about the pointer device.


## -parameters




### -param device [in]

The handle to the device.


### -param pointerDevice [out]

A <a href="https://msdn.microsoft.com/1b909caf-2d69-42b9-8d60-5d89a0286f59">POINTER_DEVICE_INFO</a> structure that contains information about the pointer device.


## -returns



If this function succeeds, it returns TRUE.
 
Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/44942954-3EA6-4C33-8CF1-E8BF72A914CB">Functions</a>
 

 

