---
UID: NS:richedit._formatrange
title: FORMATRANGE (richedit.h)
description: Information that a rich edit control uses to format its output for a particular device. This structure is used with the EM_FORMATRANGE message.
helpviewer_keywords: ["FORMATRANGE","FORMATRANGE structure [Windows Controls]","_win32_FORMATRANGE_str","_win32_FORMATRANGE_str_cpp","controls.FORMATRANGE","controls._win32_FORMATRANGE_str","richedit/FORMATRANGE"]
old-location: controls\FORMATRANGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\formatrange.htm
ms.date: 12/05/2018
ms.keywords: FORMATRANGE, FORMATRANGE structure [Windows Controls], _win32_FORMATRANGE_str, _win32_FORMATRANGE_str_cpp, controls.FORMATRANGE, controls._win32_FORMATRANGE_str, richedit/FORMATRANGE
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: FORMATRANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _formatrange
 - richedit/_formatrange
 - FORMATRANGE
 - richedit/FORMATRANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - FORMATRANGE
---

# FORMATRANGE structure


## -description

Information that a rich edit control uses to format its output for a particular device. This structure is used with the <a href="/windows/win32/controls/em-formatrange">EM_FORMATRANGE</a> message.

## -struct-fields

### -field hdcTarget

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

An HDC for the target device to format for.

### -field hdc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

A HDC for the device to render to, if <a href="/windows/win32/controls/em-formatrange">EM_FORMATRANGE</a> is being used to send the output to a device.

### -field rc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The area within the <i>rcPage</i> rectangle to render to. Units are measured in twips.

### -field rcPage

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The entire area of a page on the rendering device. Units are measured in twips.

### -field chrg

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a></b>

The range of characters to format.

## -remarks

<b>hdcTarget</b> contains the HDC to format for, which is usually the same as the HDC specified by <b>hdc</b> but can be different. For example, if you create a print preview module, <b>hdc</b> is the HDC of the window in which the output is viewed, and <b>hdcTarget</b> is the HDC for the printer. 
	

The values for <b>rc</b> and <b>rcPage</b> can be obtained by using <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>.

## -see-also

<a href="/windows/win32/controls/em-formatrange">EM_FORMATRANGE</a>
