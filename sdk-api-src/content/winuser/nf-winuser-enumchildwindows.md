---
UID: NF:winuser.EnumChildWindows
title: EnumChildWindows function
author: windows-sdk-content
description: Enumerates the child windows that belong to the specified parent window by passing the handle to each child window, in turn, to an application-defined callback function.
old-location: winmsg\enumchildwindows.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\enumchildwindows.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumChildWindows, EnumChildWindows function [Windows and Messages], _win32_EnumChildWindows, _win32_enumchildwindows_cpp, winmsg.enumchildwindows, winui._win32_enumchildwindows, winuser/EnumChildWindows
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
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - EnumChildWindows
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumChildWindows function


## -description


Enumerates the child windows that belong to the specified parent window by passing the handle to each child window, in turn, to an application-defined callback function. <b>EnumChildWindows</b> continues until the last child window is enumerated or the callback function returns <b>FALSE</b>.


## -parameters




### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the parent window whose child windows are to be enumerated. If this parameter is <b>NULL</b>, this function is equivalent to <a href="https://msdn.microsoft.com/en-us/library/ms633497(v=VS.85).aspx">EnumWindows</a>.

					
				


### -param lpEnumFunc [in]

Type: <b>WNDENUMPROC</b>

A pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms633493(v=VS.85).aspx">EnumChildProc</a>. 


### -param lParam [in]

Type: <b>LPARAM</b>

An application-defined value to be passed to the callback function. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

The return value is not used.




## -remarks



If a child window has created child windows of its own, <b>EnumChildWindows</b> enumerates those windows as well. 

A child window that is moved or repositioned in the Z order during the enumeration process will be properly enumerated. The function does not enumerate a child window that is destroyed before being enumerated or that is created during the enumeration process. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633493(v=VS.85).aspx">EnumChildProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633495(v=VS.85).aspx">EnumThreadWindows</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633497(v=VS.85).aspx">EnumWindows</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633515(v=VS.85).aspx">GetWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

