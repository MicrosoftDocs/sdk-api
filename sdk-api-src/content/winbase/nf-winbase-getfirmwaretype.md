---
UID: NF:winbase.GetFirmwareType
title: GetFirmwareType function
author: windows-sdk-content
description: Retrieves the firmware type of the local computer.
old-location: base\getfirmwaretype.htm
tech.root: sysinfo
ms.assetid: db1f6889-067a-4a5d-bbfa-5836287d08ca
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFirmwareType, GetFirmwareType function, base.getfirmwaretype, winbase/GetFirmwareType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetFirmwareType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFirmwareType function


## -description


Retrieves the firmware type of the local computer.


## -parameters




### -param FirmwareType [in, out]

A pointer to a <a href="https://msdn.microsoft.com/c058e20e-11f9-4652-b658-9fd0a43d4224">FIRMWARE_TYPE</a> enumeration.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/c058e20e-11f9-4652-b658-9fd0a43d4224">FIRMWARE_TYPE</a>
 

 

