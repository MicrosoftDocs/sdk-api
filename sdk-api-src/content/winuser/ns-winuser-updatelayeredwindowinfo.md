---
UID: NS:winuser.tagUPDATELAYEREDWINDOWINFO
title: UPDATELAYEREDWINDOWINFO (winuser.h)
description: Used by UpdateLayeredWindowIndirect to provide position, size, shape, content, and translucency information for a layered window.
helpviewer_keywords: ["*PUPDATELAYEREDWINDOWINFO","PUPDATELAYEREDWINDOWINFO","PUPDATELAYEREDWINDOWINFO structure pointer [Windows and Messages]","ULW_ALPHA","ULW_COLORKEY","ULW_EX_NORESIZE","ULW_OPAQUE","UPDATELAYEREDWINDOWINFO","UPDATELAYEREDWINDOWINFO structure [Windows and Messages]","_win32_UPDATELAYEREDWINDOWINFO","_win32_updatelayeredwindowinfo_cpp","winmsg.updatelayeredwindowinfo","winui._win32_updatelayeredwindowinfo","winuser/PUPDATELAYEREDWINDOWINFO","winuser/UPDATELAYEREDWINDOWINFO"]
old-location: winmsg\updatelayeredwindowinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\updatelayeredwindowinfo.htm
ms.date: 12/05/2018
ms.keywords: '*PUPDATELAYEREDWINDOWINFO, PUPDATELAYEREDWINDOWINFO, PUPDATELAYEREDWINDOWINFO structure pointer [Windows and Messages], ULW_ALPHA, ULW_COLORKEY, ULW_EX_NORESIZE, ULW_OPAQUE, UPDATELAYEREDWINDOWINFO, UPDATELAYEREDWINDOWINFO structure [Windows and Messages], _win32_UPDATELAYEREDWINDOWINFO, _win32_updatelayeredwindowinfo_cpp, winmsg.updatelayeredwindowinfo, winui._win32_updatelayeredwindowinfo, winuser/PUPDATELAYEREDWINDOWINFO, winuser/UPDATELAYEREDWINDOWINFO'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: UPDATELAYEREDWINDOWINFO, *PUPDATELAYEREDWINDOWINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUPDATELAYEREDWINDOWINFO
 - winuser/tagUPDATELAYEREDWINDOWINFO
 - PUPDATELAYEREDWINDOWINFO
 - winuser/PUPDATELAYEREDWINDOWINFO
 - UPDATELAYEREDWINDOWINFO
 - winuser/UPDATELAYEREDWINDOWINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - UPDATELAYEREDWINDOWINFO
---

# UPDATELAYEREDWINDOWINFO structure


## -description

Used by <a href="/previous-versions/windows/desktop/legacy/ms633557(v=vs.85)">UpdateLayeredWindowIndirect</a> to provide position, size, shape, content, and translucency information for a layered window.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size, in bytes, of this structure.

### -field hdcDst

Type: <b>HDC</b>

A handle to a DC for the screen. This handle is obtained by specifying <b>NULL</b> in this member when calling <a href="/previous-versions/windows/desktop/legacy/ms633557(v=vs.85)">UpdateLayeredWindowIndirect</a>. The handle is used for palette color matching when the window contents are updated. If <b>hdcDst</b> is <b>NULL</b>, the default palette is used.

                    

If <b>hdcSrc</b> is <b>NULL</b>, <b>hdcDst</b> must be <b>NULL</b>.

### -field pptDst

Type: <b>const <a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

The new screen position of the layered window. If the new position is unchanged from the current position, <b>pptDst</b> can be <b>NULL</b>.

### -field psize

Type: <b>const <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>*</b>

The new size of the layered window. If the size of the window will not change, this parameter can be <b>NULL</b>. If <b>hdcSrc</b> is <b>NULL</b>, <b>psize</b> must be <b>NULL</b>.

### -field hdcSrc

Type: <b>HDC</b>

A handle to the DC for the surface that defines the layered window. This handle can be obtained by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc">CreateCompatibleDC</a> function. If the shape and visual context of the window will not change, <b>hdcSrc</b> can be <b>NULL</b>.

### -field pptSrc

Type: <b>const <a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

The location of the layer in the device context. If <b>hdcSrc</b> is <b>NULL</b>, <b>pptSrc</b> should be <b>NULL</b>.

### -field crKey

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

The color key to be used when composing the layered window. To generate a <a href="/windows/desktop/gdi/colorref">COLORREF</a>, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

### -field pblend

Type: <b>const <a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a>*</b>

The transparency value to be used when composing the layered window.

### -field dwFlags

Type: <b>DWORD</b>

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ULW_ALPHA"></a><a id="ulw_alpha"></a><dl>
<dt><b>ULW_ALPHA</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Use <i>pblend</i> as the blend function. If the display mode is 256 colors or less, the effect of this value is the same as the effect of ULW_OPAQUE.

</td>
</tr>
<tr>
<td width="40%"><a id="ULW_COLORKEY"></a><a id="ulw_colorkey"></a><dl>
<dt><b>ULW_COLORKEY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Use <i>crKey</i> as the transparency color. 

</td>
</tr>
<tr>
<td width="40%"><a id="ULW_OPAQUE"></a><a id="ulw_opaque"></a><dl>
<dt><b>ULW_OPAQUE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Draw an opaque layered window. 

</td>
</tr>
<tr>
<td width="40%"><a id="ULW_EX_NORESIZE"></a><a id="ulw_ex_noresize"></a><dl>
<dt><b>ULW_EX_NORESIZE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Force the <a href="/previous-versions/windows/desktop/legacy/ms633557(v=vs.85)">UpdateLayeredWindowIndirect</a> function to fail if the current window size does not match the size specified in the <i>psize</i>. 

</td>
</tr>
</table>
 

If <b>hdcSrc</b> is <b>NULL</b>, <b>dwFlags</b> should be zero.

### -field prcDirty

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

The area to be updated. This parameter can be <b>NULL</b>. If it is non-NULL, only the area in this rectangle is updated from the source DC.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-updatelayeredwindow">UpdateLayeredWindow</a>



<a href="/windows/desktop/winmsg/window-features">Window Features</a>