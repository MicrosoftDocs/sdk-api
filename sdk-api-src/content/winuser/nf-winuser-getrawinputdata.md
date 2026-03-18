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

Retrieves the raw input data from the specified [RAWINPUT](ns-winuser-rawinput.md) handle.

## -parameters

### -param hRawInput [in]

Type: **HRAWINPUT**

A handle to the [RAWINPUT](ns-winuser-rawinput.md) structure. This handle is passed in the *lParam* of a [WM_INPUT](/windows/win32/inputdev/wm-input) message.

### -param uiCommand [in]

Type: **UINT**

The command flag specifying which part of the [RAWINPUT](ns-winuser-rawinput.md) structure to retrieve. This parameter can be one of the following values.

| Value | Meaning |
|-------|---------|
| **RID_HEADER** 0x10000005 | Retrieve only the [RAWINPUTHEADER](ns-winuser-rawinputheader.md) from the [RAWINPUT](ns-winuser-rawinput.md) structure. *pData* must point to a **RAWINPUTHEADER**-sized buffer. |
| **RID_INPUT** 0x10000003 | Retrieve the complete [RAWINPUT](ns-winuser-rawinput.md) structure including device-specific data. |

### -param pData [out, optional]

Type: **LPVOID**

A pointer to the buffer that receives the data. The type of data depends on the value of *uiCommand*: a [RAWINPUTHEADER](ns-winuser-rawinputheader.md) for **RID_HEADER**, or a complete [RAWINPUT](ns-winuser-rawinput.md) structure for **RID_INPUT**.

If **NULL**, the required size of the buffer is returned in \**pcbSize* and the function returns zero.

If the buffer is too small, the function returns (**UINT**)-1, sets **ERROR_INSUFFICIENT_BUFFER**, and returns the required size in \**pcbSize*.

### -param pcbSize [in, out]

Type: **PUINT**

On input, the size in bytes of the buffer pointed to by *pData*. On output, if the buffer is too small, receives the required size in bytes.

### -param cbSizeHeader [in]

Type: **UINT**

The size, in bytes, of the [RAWINPUTHEADER](ns-winuser-rawinputheader.md) structure. Must be `sizeof(RAWINPUTHEADER)`, otherwise the function fails with **ERROR_INVALID_PARAMETER**.

## -returns

Type: **UINT**

If *pData* is **NULL** and the function is successful, the return value is zero and \**pcbSize* contains the required buffer size.

If *pData* is not **NULL** and the function is successful, the return value is the number of bytes copied into *pData*.

If an error occurs, the return value is (**UINT**)-1. Call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) for the error code.

## -remarks

**GetRawInputData** retrieves one [RAWINPUT](ns-winuser-rawinput.md) structure at a time using the **HRAWINPUT** handle passed in *lParam* of a [WM_INPUT](/windows/win32/inputdev/wm-input) message. In contrast, [GetRawInputBuffer](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) retrieves an array of **RAWINPUT** structures accumulated in the thread's raw input queue.

**Handle lifetime:** The **HRAWINPUT** handle in *lParam* is valid for the duration of the [WM_INPUT](/windows/win32/inputdev/wm-input) message handler. It is freed internally on the next call to [GetMessage](/windows/win32/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagew) with **PM_REMOVE** via a deferred cleanup mechanism. **GetRawInputData** must be called before then.

**Relationship with GetRawInputBuffer:** [GetMessage](/windows/win32/api/winuser/nf-winuser-getmessage) removes the current [WM_INPUT](/windows/win32/inputdev/wm-input) from the raw input queue before returning. As a result, [GetRawInputBuffer](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) will not see the current event — only events that arrived after it.

See [Performing a Buffered Read of Raw Input](/windows/win32/inputdev/using-raw-input#performing-a-buffered-read-of-raw-input) for complete code samples.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/nf-winuser-getrawinputbuffer">GetRawInputBuffer</a>

<a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a>

<a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a>

<a href="/windows/desktop/inputdev/raw-input">Raw Input</a>



<b>Reference</b>
