---
UID: NF:ddrawgdi.DdCreateDIBSection
title: DdCreateDIBSection function (ddrawgdi.h)
description: Creates a DIBSECTION structure that shares its color table with the device. GdiEntry9 is defined as an alias for this function.
helpviewer_keywords: ["DdCreateDIBSection","DdCreateDIBSection function [Windows API]","GdiEntry9","_dxgkernel_ddcreatedibsection","ddrawgdi/DdCreateDIBSection","ddrawgdi/GdiEntry9","winprog._dxgkernel_ddcreatedibsection","winui._dxgkernel_ddcreatedibsection"]
old-location: winprog\_dxgkernel_ddcreatedibsection.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddcreatedibsection.htm
ms.date: 12/05/2018
ms.keywords: DdCreateDIBSection, DdCreateDIBSection function [Windows API], GdiEntry9, _dxgkernel_ddcreatedibsection, ddrawgdi/DdCreateDIBSection, ddrawgdi/GdiEntry9, winprog._dxgkernel_ddcreatedibsection, winui._dxgkernel_ddcreatedibsection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdCreateDIBSection
 - ddrawgdi/DdCreateDIBSection
dev_langs:
 - c++
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
---

# DdCreateDIBSection function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Creates a <a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a> structure that shares its color table with the device.


<b>GdiEntry9</b> is defined as an alias for this function.

## -parameters

### -param hdc

A valid DC compatible with the current display device.

### -param pbmi

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure that describes the requested <a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a>.

### -param iUsage

Specifies the type of data contained in the <b>bmiColors</b> array member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure pointed to by <i>pbmi</i> (either logical palette indexes or literal RGB values). The following values are defined.



#### (DIB_PAL_COLORS)

The <b>bmiColors</b> member is an array of 16-bit indexes into the logical palette of the device context specified by <i>hdc</i>.



#### (DIB_RGB_COLORS)

The <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure contains an array of literal RGB values.

### -param ppvBits

Pointer to a pointer to the created <a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a> data.

### -param hSectionApp

Reserved. Must be <b>NULL</b>.

### -param dwOffset

## -returns

If successful, this function returns a handle to a bitmap representing the <a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a>; otherwise it returns <b>NULL</b>.

## -remarks

Calling this function ensures an identity palette, and no palette conversion when <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-blt">IDirectDrawSurface7::Blt</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a> are called.


Applications are advised to use <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>, which can create 8-bit-per-pixel, identity-paletted surfaces in a manner independent of the operating system.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>