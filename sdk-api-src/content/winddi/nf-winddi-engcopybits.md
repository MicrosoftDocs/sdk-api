---
UID: NF:winddi.EngCopyBits
title: EngCopyBits function
author: windows-sdk-content
description: The EngCopyBits function translates between device-managed raster surfaces and GDI standard-format bitmaps.
old-location: display\engcopybits.htm
old-project: display
ms.assetid: ad8e0658-8378-4f4e-867a-6bd8a479c354
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EngCopyBits, EngCopyBits function [Display Devices], display.engcopybits, gdifncs_032d6884-2d0c-4554-a896-0fb80cfca707.xml, winddi/EngCopyBits
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
 - Ext-MS-Win-moderncore-Win32k-base-ntgdi-l1-1-0.dll
 - win32kfull.sys
 - win32kmin.sys
api_name:
 - EngCopyBits
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngCopyBits function


## -description


The <b>EngCopyBits</b> function translates between device-managed raster surfaces and GDI standard-format bitmaps.


## -parameters




### -param psoDest

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that describes the destination surface for the copy operation.


### -param psoSrc

Pointer to a SURFOBJ structure that describes the source surface for the copy operation.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure that restricts the area of the destination surface that will be affected. This parameter can be <b>NULL</b>.


### -param pxlo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a> structure that defines the translation of color indices between the source and target surfaces.


### -param prclDest [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that defines the area in the coordinate system of the destination surface that will be modified. The rectangle is lower-right exclusive, meaning the lower and right edges of this rectangle are not part of the copy.


### -param pptlSrc [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that defines the upper left corner of the source rectangle.


## -returns



The return value is <b>TRUE</b> if the function is successful. If it is unsuccessful, it logs an error and returns <b>FALSE</b>.




## -remarks



Standard-format bitmaps are single-plane, packed-pixel format. Each scan line is aligned on a 4-byte boundary. These bitmaps have 1, 4, 8, 16, 24, or 32 bits per pixel. See the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564199">EngCreateBitmap</a> function for a list of standard format types.

GDI calls this function from its simulations.

<b>EngCopyBits</b> should not be called with an empty destination rectangle, and the two points of the destination rectangle must be well-ordered; that is, the first point should represent the upper-left vertex of the rectangle, and the second should represent the lower-right vertex.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570634">XLATEOBJ</a>
 

 

