---
UID: NF:winuser.GetRawInputData
title: GetRawInputData function (winuser.h)
description: Retrieves the raw input from the specified device.
helpviewer_keywords: ["GetRawInputData","GetRawInputData function [Keyboard and Mouse Input]","RID_HEADER","RID_INPUT","_win32_GetRawInputData","_win32_getrawinputdata_cpp","inputdev.getrawinputdata","winui._win32_getrawinputdata","winuser/GetRawInputData"]
old-location: inputdev\getrawinputdata.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getrawinputdata.htm
ms.date: 12/05/2018
ms.keywords: GetRawInputData, GetRawInputData function [Keyboard and Mouse Input], RID_HEADER, RID_INPUT, _win32_GetRawInputData, _win32_getrawinputdata_cpp, inputdev.getrawinputdata, winui._win32_getrawinputdata, winuser/GetRawInputData
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetRawInputData
 - winuser/GetRawInputData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-rawinput-l1-2-0.dll
 - ext-ms-win-rtcore-ntuser-rawinput-l1-1-1.dll
 - ext-ms-win-ntuser-rawinput-l1-2-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-RTCore-NTUser-Rawinput-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetRawInputData
req.apiset: ext-ms-win-ntuser-rawinput-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# GetRawInputData function


## -description

Retrieves the raw input from the specified device.

## -parameters

### -param hRawInput [in]

Type: <b>HRAWINPUT</b>

A handle to the <a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structure. This comes from the <i>lParam</i> in <a href="/windows/desktop/inputdev/wm-input">WM_INPUT</a>.

### -param uiCommand [in]

Type: <b>UINT</b>

The command flag. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RID_HEADER"></a><a id="rid_header"></a><dl>
<dt><b>RID_HEADER</b></dt>
<dt>0x10000005</dt>
</dl>
</td>
<td width="60%">
Get the header information from the <a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="RID_INPUT"></a><a id="rid_input"></a><dl>
<dt><b>RID_INPUT</b></dt>
<dt>0x10000003</dt>
</dl>
</td>
<td width="60%">
Get the raw data from the <a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structure.

</td>
</tr>
</table>

### -param pData [out, optional]

Type: <b>LPVOID</b>

A pointer to the data that comes from the <a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structure. This depends on the value of <i>uiCommand</i>. Pointer should be aligned on a **DWORD** (32-bit) boundary. 

If <i>pData</i> is <b>NULL</b>, the required size of the buffer is returned in *<i>pcbSize</i>.

### -param pcbSize [in, out]

Type: <b>PUINT</b>

The size, in bytes, of the data in <i>pData</i>.

### -param cbSizeHeader [in]

Type: <b>UINT</b>

The size, in bytes, of the <a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a> structure.

## -returns

Type: <b>UINT</b>

If <i>pData</i> is <b>NULL</b> and the function is successful, the return value is 0. If <i>pData</i> is not <b>NULL</b> and the function is successful, the return value is the number of bytes copied into pData.

If there is an error, the return value is (<b>UINT</b>)-1.

## -remarks

<b>GetRawInputData</b> gets the raw input one <a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a> structure at a time. In contrast, <a href="/windows/desktop/api/winuser/nf-winuser-getrawinputbuffer">GetRawInputBuffer</a> gets an array of <b>RAWINPUT</b> structures.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/nf-winuser-getrawinputbuffer">GetRawInputBuffer</a>

<a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a>

<a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a>

<a href="/windows/desktop/inputdev/raw-input">Raw Input</a>



<b>Reference</b>
