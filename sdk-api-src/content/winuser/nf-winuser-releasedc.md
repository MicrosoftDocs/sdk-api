---
UID: NF:winuser.ReleaseDC
title: ReleaseDC function (winuser.h)
description: The ReleaseDC function releases a device context (DC), freeing it for use by other applications. The effect of the ReleaseDC function depends on the type of DC. It frees only common and window DCs. It has no effect on class or private DCs.
helpviewer_keywords: ["ReleaseDC","ReleaseDC function [Windows GDI]","_win32_ReleaseDC","gdi.releasedc","winuser/ReleaseDC"]
old-location: gdi\releasedc.htm
tech.root: gdi
ms.assetid: c4f48f1e-4a37-4330-908e-2ac5c65e1a1d
ms.date: 12/05/2018
ms.keywords: ReleaseDC, ReleaseDC function [Windows GDI], _win32_ReleaseDC, gdi.releasedc, winuser/ReleaseDC
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReleaseDC
 - winuser/ReleaseDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-DC-Access-Ext-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-DC-Access-l1-1-0.dll
 - minuser.dll
 - api-ms-win-ntuser-dc-access-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-DC-Access-L1-1-1.dll
api_name:
 - ReleaseDC
---

# ReleaseDC function


## -description

The <b>ReleaseDC</b> function releases a device context (DC), freeing it for use by other applications. The effect of the <b>ReleaseDC</b> function depends on the type of DC. It frees only common and window DCs. It has no effect on class or private DCs.

## -parameters

### -param hWnd [in]

A handle to the window whose DC is to be released.

### -param hDC [in]

A handle to the DC to be released.

## -returns

The return value indicates whether the DC was released. If the DC was released, the return value is 1.

If the DC was not released, the return value is zero.

## -remarks

The application must call the <b>ReleaseDC</b> function for each call to the <a href="/windows/desktop/api/winuser/nf-winuser-getwindowdc">GetWindowDC</a> function and for each call to the <a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a> function that retrieves a common DC.

An application cannot use the <b>ReleaseDC</b> function to release a DC that was created by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a> function; instead, it must use the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a> function. <b>ReleaseDC</b> must be called from the same thread that called <a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a>.


#### Examples

For an example, see <a href="/windows/desktop/gdi/scaling-an-image">Scaling an Image</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowdc">GetWindowDC</a>