---
UID: NF:winuser.GetRawPointerDeviceData
title: GetRawPointerDeviceData function
author: windows-sdk-content
description: Gets the raw input data from the pointer device.
old-location: input_pointerdevice\getrawpointerdevicedata.htm
old-project: Input_PointerDevice
ms.assetid: 56b65cc9-9582-4c7f-81e8-0b0d45b4dc8b
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: GetRawPointerDeviceData, GetRawPointerDeviceData function, input_pointerdevice.getrawpointerdevicedata, unifiedinputstack.getrawpointerdevicedata, winuser/GetRawPointerDeviceData
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
 - GetRawPointerDeviceData
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetRawPointerDeviceData function


## -description


Gets the raw input data  from the pointer device. 


## -parameters




### -param pointerId [in]

An identifier of the pointer for which to retrieve information.


### -param historyCount [in]

The pointer history.


### -param propertiesCount [in]

Number of properties to retrieve.


### -param pProperties [in]

Array of <a href="https://msdn.microsoft.com/2c96379e-7c9f-440c-a98b-bda38bacd33f">POINTER_DEVICE_PROPERTY</a> structures that contain raw data reported by the device.


### -param pValues [out]

The values for <i>pProperties</i>.


## -returns



TRUE if the function succeeds; otherwise, FALSE. If the function fails, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

