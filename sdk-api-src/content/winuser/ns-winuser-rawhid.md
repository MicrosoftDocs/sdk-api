---
UID: NS:winuser.tagRAWHID
title: RAWHID (winuser.h)
description: Describes the format of the raw input from a Human Interface Device (HID).
helpviewer_keywords: ["*LPRAWHID","*PRAWHID","LPRAWHID","LPRAWHID structure pointer [Keyboard and Mouse Input]","PRAWHID","PRAWHID structure pointer [Keyboard and Mouse Input]","RAWHID","RAWHID structure [Keyboard and Mouse Input]","_win32_RAWHID_str","_win32_rawhid_str_cpp","inputdev.rawhid","winui._win32_rawhid_str","winuser/LPRAWHID","winuser/PRAWHID","winuser/RAWHID"]
old-location: inputdev\rawhid.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawhid.htm
ms.date: 12/05/2018
ms.keywords: '*LPRAWHID, *PRAWHID, LPRAWHID, LPRAWHID structure pointer [Keyboard and Mouse Input], PRAWHID, PRAWHID structure pointer [Keyboard and Mouse Input], RAWHID, RAWHID structure [Keyboard and Mouse Input], _win32_RAWHID_str, _win32_rawhid_str_cpp, inputdev.rawhid, winui._win32_rawhid_str, winuser/LPRAWHID, winuser/PRAWHID, winuser/RAWHID'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: RAWHID, *PRAWHID, *LPRAWHID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRAWHID
 - winuser/tagRAWHID
 - PRAWHID
 - winuser/PRAWHID
 - RAWHID
 - winuser/RAWHID
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
 - RAWHID
---

# RAWHID structure


## -description

Describes the format of the raw input from a Human Interface Device (HID).

## -struct-fields

### -field dwSizeHid

Type: <b>DWORD</b>

The size, in bytes, of each HID input in <b>bRawData</b>.

### -field dwCount

Type: <b>DWORD</b>

The number of HID inputs in <b>bRawData</b>.

### -field bRawData

Type: <b>BYTE[1]</b>

The raw input data, as an array of bytes.

## -remarks

Each <a href="/windows/desktop/inputdev/wm-input">WM_INPUT</a> can indicate several inputs, but all of the inputs come from the same HID. The size of the <b>bRawData</b> array is <b>dwSizeHid</b> *	<b>dwCount</b>.

For more information, see <a href="/windows-hardware/drivers/hid/interpreting-hid-reports">Interpreting HID Reports</a>.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a>

<a href="/windows/desktop/inputdev/raw-input">Raw Input</a>

<a href="/windows-hardware/drivers/hid/">Introduction to Human Interface Devices (HID)</a>

<b>Reference</b>

<a href="/windows/desktop/inputdev/wm-input">WM_INPUT</a>

<a href="/windows-hardware/drivers/hid/interpreting-hid-reports">Interpreting HID Reports</a>