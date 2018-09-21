---
UID: NF:winuser.GetAltTabInfoA
title: GetAltTabInfoA function
author: windows-sdk-content
description: Retrieves status information for the specified window if it is the application-switching (ALT+TAB) window.
old-location: winmsg\getalttabinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getalttabinfo.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetAltTabInfo, GetAltTabInfo function [Windows and Messages], GetAltTabInfoA, GetAltTabInfoW, _win32_GetAltTabInfo, _win32_getalttabinfo_cpp, winmsg.getalttabinfo, winui._win32_getalttabinfo, winuser/GetAltTabInfo, winuser/GetAltTabInfoA, winuser/GetAltTabInfoW
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
req.unicode-ansi: GetAltTabInfoW (Unicode) and GetAltTabInfoA (ANSI)
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
api_name:
 - GetAltTabInfo
 - GetAltTabInfoA
 - GetAltTabInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetAltTabInfoA function


## -description


Retrieves status information for the specified window if it is the application-switching (ALT+TAB) window.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the window for which status information will be retrieved. This window must be the application-switching window. 


### -param iItem [in]

Type: <b>int</b>

The index of the icon in the application-switching window. If the <i>pszItemText</i> parameter is not <b>NULL</b>, the name of the item is copied to the <i>pszItemText</i> string. If this parameter is –1, the name of the item is not copied. 


### -param pati [in, out]

Type: <b>PALTTABINFO</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms632601(v=VS.85).aspx">ALTTABINFO</a> structure to receive the status information. Note that you must set the <b>csSize</b> member to <code>sizeof(ALTTABINFO)</code> before calling this function. 


### -param pszItemText [out, optional]

Type: <b>LPTSTR</b>

The name of the item. If this parameter is <b>NULL</b>, the name of the item is not copied. 


### -param cchItemText [in]

Type: <b>UINT</b>

The size, in characters, of the <i>pszItemText</i> buffer. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The application-switching window enables you to switch to the most recently used application window. To display the application-switching window, press ALT+TAB. To select an application from the list, continue to hold ALT down and press TAB to move through the list. Add SHIFT to reverse direction through the list.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms632601(v=VS.85).aspx">ALTTABINFO</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

