---
UID: NF:winuser.GetClassNameA
title: GetClassNameA function
author: windows-sdk-content
description: Retrieves the name of the class to which the specified window belongs.
old-location: winmsg\getclassname.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getclassname.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetClassName, GetClassName function [Windows and Messages], GetClassNameA, GetClassNameW, _win32_GetClassName, _win32_getclassname_cpp, winmsg.getclassname, winui._win32_getclassname, winuser/GetClassName, winuser/GetClassNameA, winuser/GetClassNameW
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
req.unicode-ansi: GetClassNameW (Unicode) and GetClassNameA (ANSI)
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
 - Ext-MS-Win-NTUser-Windowclass-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - GetClassName
 - GetClassNameA
 - GetClassNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClassNameA function


## -description


Retrieves the name of the class to which the specified window belongs. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs. 


### -param lpClassName [out]

Type: <b>LPTSTR</b>

The class name string.


### -param nMaxCount [in]

Type: <b>int</b>

The length
					
					 of the 
					<i>lpClassName</i> buffer, in 
	

					characters. The buffer must be large enough to include the terminating null character; otherwise, the class name string is truncated to <code>nMaxCount-1</code> characters.


## -returns



Type: <strong>Type: <b>int</b>
</strong>

If the function succeeds, the return value is the number of 
						characters copied to the buffer, not including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633499(v=VS.85).aspx">FindWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633578(v=VS.85).aspx">GetClassInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633580(v=VS.85).aspx">GetClassLong</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633583(v=VS.85).aspx">GetClassWord</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632596(v=VS.85).aspx">Window Classes</a>
 

 

