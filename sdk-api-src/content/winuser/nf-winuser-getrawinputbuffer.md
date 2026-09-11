---
UID: NF:winuser.GetRawInputBuffer
title: GetRawInputBuffer function (winuser.h)
description: Performs a buffered read of the raw input data.
helpviewer_keywords: ["GetRawInputBuffer","GetRawInputBuffer function [Keyboard and Mouse Input]","_win32_GetRawInputBuffer","_win32_getrawinputbuffer_cpp","inputdev.getrawinputbuffer","winui._win32_getrawinputbuffer","winuser/GetRawInputBuffer"]
old-location: inputdev\getrawinputbuffer.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getrawinputbuffer.htm
ms.date: 12/05/2018
ms.keywords: GetRawInputBuffer, GetRawInputBuffer function [Keyboard and Mouse Input], _win32_GetRawInputBuffer, _win32_getrawinputbuffer_cpp, inputdev.getrawinputbuffer, winui._win32_getrawinputbuffer, winuser/GetRawInputBuffer
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
 - GetRawInputBuffer
 - winuser/GetRawInputBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetRawInputBuffer
---

# GetRawInputBuffer function

## -description

Performs a buffered read of the raw input messages data found in the calling thread's message queue.

## -parameters

### -param pData [out, optional]

Type: **PRAWINPUT**

A pointer to a buffer of [RAWINPUT](ns-winuser-rawinput.md) structures that contain the raw input data. The pointer must be aligned on a **DWORD** (32-bit) boundary on 32-bit systems, and on a **QWORD** (64-bit) boundary on 64-bit systems.

If **NULL**, the size of the first pending raw input message, in bytes, is returned in \**pcbSize*. The queue is not modified.

### -param pcbSize [in, out]

Type: **PUINT**

The size, in bytes, of the provided [RAWINPUT](ns-winuser-rawinput.md) buffer. On return, contains the size of the first element that did not fit, or zero if all elements were read.

### -param cbSizeHeader [in]

Type: **UINT**

The size, in bytes, of the [RAWINPUTHEADER](ns-winuser-rawinputheader.md) structure.

## -returns

Type: **UINT**

If *pData* is **NULL** and the function is successful, the return value is zero. If *pData* is not **NULL** and the function is successful, the return value is the number of [RAWINPUT](ns-winuser-rawinput.md) structures written to *pData*.

If an error occurs, the return value is (**UINT**)-1. Call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) for the error code. A common error is **ERROR_INSUFFICIENT_BUFFER**, which means the buffer is too small to hold the first pending element — in this case \**pcbSize* is updated with the required size and the function should be retried with a larger buffer.

## -remarks

When an application receives raw input, its message queue gets a [WM_INPUT](/windows/win32/inputdev/wm-input) message and the queue status flag [QS_RAWINPUT](nf-winuser-getqueuestatus.md) is set.

**GetRawInputBuffer** reads [WM_INPUT](/windows/win32/inputdev/wm-input) messages directly from the calling thread's raw input queue and removes them as they are read. You can call this function several times until all raw input messages have been read. When all messages have been successfully read and *pData* is not **NULL**, the [QS_RAWINPUT](nf-winuser-getqueuestatus.md) flag is cleared from the calling thread's message queue status.

The [NEXTRAWINPUTBLOCK](nf-winuser-nextrawinputblock.md) macro allows an application to traverse an array of [RAWINPUT](ns-winuser-rawinput.md) structures.

**Important:** **GetRawInputBuffer** only sees [WM_INPUT](/windows/win32/inputdev/wm-input) messages that are still present in the raw input queue. When [GetMessage](nf-winuser-getmessage.md) retrieves a [WM_INPUT](/windows/win32/inputdev/wm-input) message, it removes that message from the queue before returning — so **GetRawInputBuffer** will not see it. The removed event must be read via [GetRawInputData](nf-winuser-getrawinputdata.md) using the **HRAWINPUT** handle passed in *lParam*. Only events that arrived after the current one are visible to **GetRawInputBuffer**.

Therefore, when using **GetRawInputBuffer** from a [WM_INPUT](/windows/win32/inputdev/wm-input) handler or after [GetMessage](nf-winuser-getmessage.md), the correct pattern is:

1. Read the current event via [GetRawInputData](nf-winuser-getrawinputdata.md) using the *lParam* handle.
2. Call **GetRawInputBuffer** in a loop to drain any additional events that accumulated in the queue.
3. Call [DefWindowProc](/windows/win32/api/winproc/nf-winproc-defwndproc) after processing the message.

See [Performing a Buffered Read of Raw Input](/windows/win32/inputdev/using-raw-input#performing-a-buffered-read-of-raw-input) for complete code samples.

> [!NOTE]
> WOW64: To get the correct size of the raw input buffer, do not use \**pcbSize*, use \**pcbSize* \* 8 instead. To ensure **GetRawInputBuffer** behaves properly on WOW64, you must align the [RAWINPUT](ns-winuser-rawinput.md) structure by 8 bytes. The following code shows how to align **RAWINPUT** for WOW64.

```csharp
[StructLayout(LayoutKind.Explicit)]
internal struct RAWINPUT
{
    [FieldOffset(0)]
    public RAWINPUTHEADER header;

    [FieldOffset(16+8)]
    public RAWMOUSE mouse;

    [FieldOffset(16+8)]
    public RAWKEYBOARD keyboard;

    [FieldOffset(16+8)]
    public RAWHID hid;
}
```

## -see-also

**Conceptual** 

[GetMessage](nf-winuser-getmessage.md)

[GetRawInputData](nf-winuser-getrawinputdata.md)

[NEXTRAWINPUTBLOCK](nf-winuser-nextrawinputblock.md)

[RAWINPUT](ns-winuser-rawinput.md)

[RAWINPUTHEADER](ns-winuser-rawinputheader.md)

[Raw Input](/windows/win32/inputdev/raw-input)

**Reference**

[Raw Input Overview](/windows/win32/inputdev/about-raw-input)
