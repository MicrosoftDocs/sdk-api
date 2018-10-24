---
UID: NF:winddi.EngCreateDeviceBitmap
title: EngCreateDeviceBitmap function
author: windows-sdk-content
description: The EngCreateDeviceBitmap function requests GDI to create a handle for a device bitmap.
old-location: display\engcreatedevicebitmap.htm
tech.root: display
ms.assetid: dc9d7154-30b9-4462-9161-6df03946308d
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: EngCreateDeviceBitmap, EngCreateDeviceBitmap function [Display Devices], display.engcreatedevicebitmap, gdifncs_e802b5e9-a939-4aa4-b4df-82172e825fa5.xml, winddi/EngCreateDeviceBitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngCreateDeviceBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngCreateDeviceBitmap function


## -description


The <b>EngCreateDeviceBitmap</b> function requests GDI to create a handle for a device bitmap.


## -parameters




### -param dhsurf [in]

Device handle to the device bitmap to be created.


### -param sizl [in]

Specifies a SIZEL structure that contains the width and height of the bitmap to be created. The <b>cx</b> and <b>cy</b> members of this structure contain respectively, the bitmap's width and height, in pixels. A SIZEL structure is identical to a <a href="https://msdn.microsoft.com/08d81096-069f-4554-9bb9-d4a37c0950ac">SIZE</a> structure.


### -param iFormatCompat

Specifies the compatible engine format of the device surface being created. This is used by GDI if a temporary buffer is needed to simulate a complicated drawing call. The allowable values for <i>iFormatCompat</i> are BMF_1BPP, BMF_4BPP, BMF_8BPP, BMF_16BPP, BMF_24BPP, and BMF_32BPP.


## -returns



The return value is a handle that identifies the bitmap if the function is successful. Otherwise, it is zero, and an error code is logged.




## -remarks



The surface should be associated by using <a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a>. The bitmap should be deleted by calling <a href="https://msdn.microsoft.com/9cde6fa3-26b6-49fd-9374-cbf91215aa39">EngDeleteSurface</a> when it is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/51da3fbc-bf6e-47a9-8ee8-ebf34c23b66c">EngCreateBitmap</a>
 

 

