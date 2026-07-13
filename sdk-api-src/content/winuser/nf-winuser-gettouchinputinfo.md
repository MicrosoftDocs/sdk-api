---
UID: NF:winuser.GetTouchInputInfo
title: GetTouchInputInfo function (winuser.h)
description: Retrieves detailed information about touch inputs associated with a particular touch input handle.
helpviewer_keywords: ["GetTouchInputInfo","GetTouchInputInfo function [Windows Touch]","wintouch.gettouchinputinfo","winuser/GetTouchInputInfo"]
old-location: wintouch\gettouchinputinfo.htm
tech.root: wintouch
ms.assetid: 18caab11-9c22-46ac-b89f-dd3e662bea1e
ms.date: 12/05/2018
ms.keywords: GetTouchInputInfo, GetTouchInputInfo function [Windows Touch], wintouch.gettouchinputinfo, winuser/GetTouchInputInfo
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - GetTouchInputInfo
 - winuser/GetTouchInputInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - user32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetTouchInputInfo
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# GetTouchInputInfo function


## -description

Retrieves detailed information about touch inputs associated with a particular touch input handle.

## -parameters

### -param hTouchInput [in]

The touch input handle received in the <b>LPARAM</b> of a touch message. The function fails with <b>ERROR_INVALID_HANDLE</b> if this handle is not valid. Note that the handle is not valid after it has been used in a successful call to <a href="/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle">CloseTouchInputHandle</a> or after it has been passed to <a href="/windows/desktop/wintouch/sendmessage--postmessage--and-related-functions">DefWindowProc, PostMessage, SendMessage</a> or one of their variants.

### -param cInputs [in]

The number of structures in the <i>pInputs</i> array. This should ideally be at least equal to the number of touch points associated with the message as indicated in the message <b>WPARAM</b>. If <i>cInputs</i> is less than the number of touch points, the function will still succeed and populate the <i>pInputs</i> buffer with information about <i>cInputs</i> touch points.

### -param pInputs [out]

A pointer to an array of <a href="/windows/desktop/api/winuser/ns-winuser-touchinput">TOUCHINPUT</a> structures to receive information about the touch points associated with the specified touch input handle.

### -param cbSize [in]

The size, in bytes, of a single <a href="/windows/desktop/api/winuser/ns-winuser-touchinput">TOUCHINPUT</a> structure. If <i>cbSize</i> is not the size of a single <b>TOUCHINPUT</b> structure, the function fails with <b>ERROR_INVALID_PARAMETER</b>.

## -returns

If the function succeeds, the return value is nonzero.
If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

Calling <a href="/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle">CloseTouchInputHandle</a> will not free memory associated with values retrieved in a call to <b>GetTouchInputInfo</b>.  Values in structures passed to <b>GetTouchInputInfo</b>  will be valid until you delete them.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle">CloseTouchInputHandle</a>



<a href="/windows/desktop/wintouch/mtfunctions">Functions</a>



<a href="/windows/desktop/api/winuser/ns-winuser-touchinput">TOUCHINPUT</a>
