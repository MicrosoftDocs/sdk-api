---
UID: NF:ddraw.DirectDrawEnumerateExW
title: DirectDrawEnumerateExW function
author: windows-sdk-content
description: Enumerates all DirectDraw devices that are installed on the computer. The NULL entry always identifies the primary display device that is shared with GDI.
old-location: directdraw\directdrawenumerateex.htm
old-project: directdraw
ms.assetid: 38edfaaf-2c19-4836-b662-343312220032
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DDENUM_ATTACHEDSECONDARYDEVICES, DDENUM_DETACHEDSECONDARYDEVICES, DDENUM_NONDISPLAYDEVICES, DirectDrawEnumerateEx, DirectDrawEnumerateEx function [DirectDraw], DirectDrawEnumerateExA, DirectDrawEnumerateExW, ddraw/DirectDrawEnumerateEx, ddraw/DirectDrawEnumerateExA, ddraw/DirectDrawEnumerateExW, directdraw.directdrawenumerateex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ddraw.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DirectDrawEnumerateExW (Unicode) and DirectDrawEnumerateExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ddraw.dll
 - Ext-MS-Win-DX-DDraw-L1-1-0.dll
api_name:
 - DirectDrawEnumerateEx
 - DirectDrawEnumerateExA
 - DirectDrawEnumerateExW
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# DirectDrawEnumerateExW function


## -description


Enumerates all DirectDraw devices that are installed on the computer. The NULL entry always identifies the primary display device that is shared with GDI.



## -parameters




### -param lpCallback [in]

Address of a <a href="https://msdn.microsoft.com/D3D31978-D450-40B3-8C61-1F2662C1BA50">DDEnumCallbackEx</a> function to be called with a description of each enumerated DirectDraw-enabled hardware abstraction layer (HAL).


### -param lpContext [in]

Address of an application-defined value to be passed to the enumeration callback function each time that it is called.


### -param dwFlags [in]

Flags that specify the enumeration scope. This parameter can be 0 or a combination of the following flags. If the value is 0, the function enumerates only the primary display device.



#### DDENUM_ATTACHEDSECONDARYDEVICES

The function enumerates the primary device and any display devices that are attached to the desktop.



#### DDENUM_DETACHEDSECONDARYDEVICES

The function enumerates the primary device and any display devices that are not attached to the desktop.



#### DDENUM_NONDISPLAYDEVICES

The function enumerates the primary device and any nondisplay devices, such as 3-D accelerators that have no 2-D capabilities.


##### - dwFlags.DDENUM_ATTACHEDSECONDARYDEVICES

The function enumerates the primary device and any display devices that are attached to the desktop.


##### - dwFlags.DDENUM_DETACHEDSECONDARYDEVICES

The function enumerates the primary device and any display devices that are not attached to the desktop.


##### - dwFlags.DDENUM_NONDISPLAYDEVICES

The function enumerates the primary device and any nondisplay devices, such as 3-D accelerators that have no 2-D capabilities.


## -returns



If the function succeeds, the return value is <b>DD_OK</b>.



If it fails, the function returns <b>DDERR_INVALIDPARAMS</b>.




## -remarks



On computers with multiple monitors, <b>DirectDrawEnumerateEx</b> enumerates multiple display devices. 



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll. To retrieve the address of the <b>DirectDrawEnumerateEx</b> function, call the <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> Win32 function with the "DirectDrawEnumerateExA" (ANSI) or "DirectDrawEnumerateExW" (Unicode) process name strings.



