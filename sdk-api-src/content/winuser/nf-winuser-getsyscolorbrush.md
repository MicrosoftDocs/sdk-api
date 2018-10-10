---
UID: NF:winuser.GetSysColorBrush
title: GetSysColorBrush function
author: windows-sdk-content
description: The GetSysColorBrush function retrieves a handle identifying a logical brush that corresponds to the specified color index.
old-location: gdi\getsyscolorbrush.htm
tech.root: gdi
ms.assetid: 07a1d8e3-eae8-40ab-9d0f-4efa9fac0117
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSysColorBrush, GetSysColorBrush function [Windows GDI], _win32_GetSysColorBrush, gdi.getsyscolorbrush, winuser/GetSysColorBrush
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - GetSysColorBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSysColorBrush function


## -description


The <b>GetSysColorBrush</b> function retrieves a handle identifying a logical brush that corresponds to the specified color index.


## -parameters




### -param nIndex [in]

A color index. This value corresponds to the color used to paint one of the window elements. See <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> for system color index values.


## -returns



The return value identifies a logical brush if the <i>nIndex</i> parameter is supported by the current platform. Otherwise, it returns <b>NULL</b>.




## -remarks



A brush is a bitmap that the system uses to paint the interiors of filled shapes. An application can retrieve the current system colors by calling the <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> function. An application can set the current system colors by calling the <a href="https://msdn.microsoft.com/41a7a96c-f9d1-44e3-a7e1-fd7d155c4ed0">SetSysColors</a> function.

An application must not register a window class for a window using a system brush. To register a window class with a system color, see the documentation of the <b>hbrBackground</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms633576(v=VS.85).aspx">WNDCLASS</a> or <a href="https://msdn.microsoft.com/en-us/library/ms633577(v=VS.85).aspx">WNDCLASSEX</a> structures.

System color brushes track changes in system colors. In other words, when the user changes a system color, the associated system color brush automatically changes to the new color.

To paint with a system color brush, an application should use <b>GetSysColorBrush</b> (nIndex) instead of <a href="https://msdn.microsoft.com/e39b5f77-97d8-4ea6-8277-7da12b3367f3">CreateSolidBrush</a> ( <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> (nIndex)), because <b>GetSysColorBrush</b> returns a cached brush instead of allocating a new one.

System color brushes are owned by the system so you don't need to destroy them. Although you don't need to delete the logical brush that <b>GetSysColorBrush</b> returns, no harm occurs by calling <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>.




## -see-also




<a href="https://msdn.microsoft.com/617eb778-876c-4bbb-90da-c5f13359becb">Brush Functions</a>



<a href="https://msdn.microsoft.com/b8912842-87d6-4d97-83ce-53d18cbedc74">Brushes Overview</a>



<a href="https://msdn.microsoft.com/e39b5f77-97d8-4ea6-8277-7da12b3367f3">CreateSolidBrush</a>



<a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>



<a href="https://msdn.microsoft.com/41a7a96c-f9d1-44e3-a7e1-fd7d155c4ed0">SetSysColors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633576(v=VS.85).aspx">WNDCLASS</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633577(v=VS.85).aspx">WNDCLASSEX</a>
 

 

