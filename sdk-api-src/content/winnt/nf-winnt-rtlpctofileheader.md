---
UID: NF:winnt.RtlPcToFileHeader
title: RtlPcToFileHeader function
author: windows-sdk-content
description: Retrieves the base address of the image that contains the specified PC value.
old-location: base\rtlpctofileheader.htm
tech.root: debug
ms.assetid: 690c9f20-d471-49c9-a40c-28926f03acac
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: RtlPcToFileHeader, RtlPcToFileHeader function, base.rtlpctofileheader, winnt/RtlPcToFileHeader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - API-MS-Win-Core-rtlsupport-l1-1-0.dll
 - ntdll.dll
 - API-MS-Win-Core-rtlsupport-l1-2-0.dll
api_name:
 - RtlPcToFileHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RtlPcToFileHeader
: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of Windows Server 2003
---

# RtlPcToFileHeader function


## -description


Retrieves the base address of the image that contains the specified PC value.


## -parameters




### -param PcValue [in]

The PC value. The function searches all modules mapped into the address space of the calling process for a module that contains this value.


### -param BaseOfImage [out]

The base address of the image containing the PC value. This value must be added to any relative addresses in the headers to locate the image.


## -returns



If the PC value is found, the function returns the base address of the image that contains the PC value.

If no image contains the PC value, the function returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/624b97fb-0453-4f47-b6bd-92aa14705e78">RtlLookupFunctionEntry</a>
 

 

