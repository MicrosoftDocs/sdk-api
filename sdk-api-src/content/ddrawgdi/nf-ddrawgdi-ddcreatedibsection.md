---
UID: NF:ddrawgdi.DdCreateDIBSection
title: DdCreateDIBSection function
author: windows-sdk-content
description: Creates a DIBSECTION structure that shares its color table with the device. GdiEntry9 is defined as an alias for this function.
old-location: winprog\_dxgkernel_ddcreatedibsection.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddcreatedibsection.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DdCreateDIBSection, DdCreateDIBSection function [Windows API], GdiEntry9, _dxgkernel_ddcreatedibsection, ddrawgdi/DdCreateDIBSection, ddrawgdi/GdiEntry9, winprog._dxgkernel_ddcreatedibsection, winui._dxgkernel_ddcreatedibsection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ddrawgdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - DllExport
api_location:
 - Ddrawgdi.h
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - DdCreateDIBSection
 - GdiEntry9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdCreateDIBSection function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Creates a <a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a> structure that shares its color table with the device.


<b>GdiEntry9</b> is defined as an alias for this function.


## -parameters




### -param hdc

A valid DC compatible with the current display device.


### -param pbmi

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure that describes the requested <a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a>.


### -param iUsage

Specifies the type of data contained in the <b>bmiColors</b> array member of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure pointed to by <i>pbmi</i> (either logical palette indexes or literal RGB values). The following values are defined.



#### (DIB_PAL_COLORS)

The <b>bmiColors</b> member is an array of 16-bit indexes into the logical palette of the device context specified by <i>hdc</i>.



#### (DIB_RGB_COLORS)

The <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure contains an array of literal RGB values.


### -param ppvBits

Pointer to a pointer to the created <a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a> data.


### -param hSectionApp

Reserved. Must be <b>NULL</b>.


### -param dwOffset


## -returns



If successful, this function returns a handle to a bitmap representing the <a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a>; otherwise it returns <b>NULL</b>.




## -remarks



Calling this function ensures an identity palette, and no palette conversion when <a href="https://msdn.microsoft.com/e458c430-855c-419b-aa50-144d2b422e78">IDirectDrawSurface7::Blt</a> or <a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a> are called.


Applications are advised to use <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>, which can create 8-bit-per-pixel, identity-paletted surfaces in a manner independent of the operating system.





## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

