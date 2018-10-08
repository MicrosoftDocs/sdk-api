---
UID: NF:winuser.GetPointerDevices
title: GetPointerDevices function
author: windows-sdk-content
description: Gets information about the pointer devices attached to the system.
old-location: input_pointerdevice\getpointerdevices.htm
tech.root: Input_PointerDevice
ms.assetid: 91FD5EBA-EDD7-4D7D-ABF3-3CE2461417B0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetPointerDevices, GetPointerDevices function, input_pointerdevice.getpointerdevices, unifiedinputstack.getpointerdevices, winuser/GetPointerDevices
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
 - GetPointerDevices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPointerDevices function


## -description


Gets information about the pointer devices attached to the system.


## -parameters




### -param deviceCount [in, out]

If <i>pointerDevices</i> is NULL, <i>deviceCount</i> returns the total number of attached pointer devices. Otherwise, <i>deviceCount</i> specifies the number of <a href="https://msdn.microsoft.com/1b909caf-2d69-42b9-8d60-5d89a0286f59">POINTER_DEVICE_INFO</a> structures pointed to by <i>pointerDevices</i>.


### -param pointerDevices [out, optional]

Array of <a href="https://msdn.microsoft.com/1b909caf-2d69-42b9-8d60-5d89a0286f59">POINTER_DEVICE_INFO</a> structures for the pointer devices attached to the system. If NULL, the total number of attached pointer devices is returned in <i>deviceCount</i>.


## -returns



If this function succeeds, it returns TRUE.
 
Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



Windows 8 supports the following:

<ul>
<li>256 contacts per pointer device.</li>
<li>2560 total contacts per system session, regardless of the number of attached devices. For example, 10 pointer devices with 256 contacts each, 20 pointer devices with 128 contacts each, and so on.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44942954-3EA6-4C33-8CF1-E8BF72A914CB">Functions</a>
 

 

