---
UID: NF:winuser.GetDpiForSystem
title: GetDpiForSystem function (winuser.h)
description: Returns the system DPI.
helpviewer_keywords: ["GetDpiForSystem","GetDpiForSystem function [High DPI]","hidpi.getdpiforsystem","winuser/GetDpiForSystem"]
old-location: hidpi\getdpiforsystem.htm
tech.root: hidpi
ms.assetid: B744EC4A-DB78-4654-B50F-C27CB7702899
ms.date: 12/05/2018
ms.keywords: GetDpiForSystem, GetDpiForSystem function [High DPI], hidpi.getdpiforsystem, winuser/GetDpiForSystem
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - GetDpiForSystem
 - winuser/GetDpiForSystem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-2.dll
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-1.dll
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetDpiForSystem
---

# GetDpiForSystem function


## -description

Returns the system DPI.



## -returns

The system DPI value.

## -remarks

The return value will be dependent based upon the calling context. If the current thread has a <a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a> value of <b>DPI_AWARENESS_UNAWARE</b>, the return value will be 96. That is because the current context always assumes a DPI of 96. For any other <b>DPI_AWARENESS</b> value, the return value will be the actual system DPI.

You should not cache the system DPI, but should use <b>GetDpiForSystem</b> whenever you need the system DPI value.

## -see-also

<a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a>
