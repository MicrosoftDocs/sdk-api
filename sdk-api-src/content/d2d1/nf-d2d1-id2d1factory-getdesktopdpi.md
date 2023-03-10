---
UID: NF:d2d1.ID2D1Factory.GetDesktopDpi
title: ID2D1Factory::GetDesktopDpi (d2d1.h)
description: Retrieves the current desktop dots per inch (DPI). To refresh this value, call ReloadSystemMetrics.
helpviewer_keywords: ["GetDesktopDpi","GetDesktopDpi method [Direct2D]","GetDesktopDpi method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","GetDesktopDpi method","ID2D1Factory.GetDesktopDpi","ID2D1Factory::GetDesktopDpi","d2d1/ID2D1Factory::GetDesktopDpi","direct2d.ID2D1Factory_GetDesktopDpi"]
old-location: direct2d\ID2D1Factory_GetDesktopDpi.htm
tech.root: Direct2D
ms.assetid: dd46252b-80eb-42c2-a2b4-5c49ef124bd5
ms.date: 05/25/2022
ms.keywords: GetDesktopDpi, GetDesktopDpi method [Direct2D], GetDesktopDpi method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],GetDesktopDpi method, ID2D1Factory.GetDesktopDpi, ID2D1Factory::GetDesktopDpi, d2d1/ID2D1Factory::GetDesktopDpi, direct2d.ID2D1Factory_GetDesktopDpi
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory::GetDesktopDpi
 - d2d1/ID2D1Factory::GetDesktopDpi
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory.GetDesktopDpi
---

## -description

> [!IMPORTANT]
> **ID2D1Factory::GetDesktopDpi** is deprecated. For a desktop app, instead use [GetDpiForWindow](/windows/win32/api/winuser/nf-winuser-getdpiforwindow). For a Universal Windows Platform (UWP) app, instead use [DisplayInformation::LogicalDpi](/uwp/api/windows.graphics.display.displayinformation.logicaldpi).

Retrieves the current desktop dots per inch (DPI). To refresh this value, call [ReloadSystemMetrics](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-reloadsystemmetrics).

## -parameters

### -param dpiX [out]

Type: <b>FLOAT*</b>

When this method returns, contains the horizontal DPI of the desktop. You must allocate storage for this parameter.

### -param dpiY [out]

Type: <b>FLOAT*</b>

When this method returns, contains the vertical DPI of the desktop. You must allocate storage for this parameter.

## -remarks

Use this method to obtain the system DPI when setting physical pixel values, such as when you specify the size of a window.

## -see-also

* [GetDpiForWindow](/windows/win32/api/winuser/nf-winuser-getdpiforwindow)
* [ID2D1Factory](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
* [How to ensure that your application displays properly on a high-DPI display](/windows/win32/Direct2D/how-to--size-a-window-properly-for-high-dpi-displays)
