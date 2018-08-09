---
UID: NF:winuser.RegisterClassExA
title: RegisterClassExA function
author: windows-sdk-content
description: Registers a window class for subsequent use in calls to the CreateWindow or CreateWindowEx function.
old-location: winmsg\registerclassex.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\registerclassex.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RegisterClassEx, RegisterClassEx function [Windows and Messages], RegisterClassExA, RegisterClassExW, _win32_RegisterClassEx, _win32_registerclassex_cpp, winmsg.registerclassex, winui._win32_registerclassex, winuser/RegisterClassEx, winuser/RegisterClassExA, winuser/RegisterClassExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegisterClassExW (Unicode) and RegisterClassExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
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
 - RegisterClassEx
 - RegisterClassExA
 - RegisterClassExW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegisterClassExA function


## -description


Registers a window class for subsequent use in calls to the <a href="https://msdn.microsoft.com/en-us/library/ms632679(v=VS.85).aspx">CreateWindow</a> or <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> function. 


## -parameters




### -param WNDCLASSEXA

TBD




#### - WNDCLASSEXW [in]

Type: <b>const WNDCLASSEX*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms633577(v=VS.85).aspx">WNDCLASSEX</a> structure. You must fill the structure with the appropriate class attributes before passing it to the function. 


## -returns



Type: <strong>Type: <b>ATOM</b>
</strong>

If the function succeeds, the return value is a class atom that uniquely identifies the class being registered. This atom can only be used by the <a href="https://msdn.microsoft.com/en-us/library/ms632679(v=VS.85).aspx">CreateWindow</a>, <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms633578(v=VS.85).aspx">GetClassInfo</a>, <a href="https://msdn.microsoft.com/en-us/library/ms633579(v=VS.85).aspx">GetClassInfoEx</a>, <a href="https://msdn.microsoft.com/en-us/library/ms633499(v=VS.85).aspx">FindWindow</a>, <a href="https://msdn.microsoft.com/en-us/library/ms633500(v=VS.85).aspx">FindWindowEx</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms644899(v=VS.85).aspx">UnregisterClass</a> functions and the <b>IActiveIMMap::FilterClientWindows</b> method. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If you register the window class by using 
				<b>RegisterClassExA</b>, the application tells the system that the windows of the created class expect messages with text or character parameters to use the ANSI character set; if you register it by using 
				<b>RegisterClassExW</b>, the application requests that the system pass text parameters of messages as Unicode. The <a href="https://msdn.microsoft.com/en-us/library/ms633529(v=VS.85).aspx">IsWindowUnicode</a> function enables applications to query the nature of each window. For more information on ANSI and Unicode functions, see <a href="https://msdn.microsoft.com/601d24b0-11bb-48fa-a257-207c3acee226">Conventions for Function Prototypes</a>.

All window classes that an application registers are unregistered when it terminates. 

No window classes registered by a DLL are unregistered when the DLL is unloaded. A DLL must explicitly unregister its classes when it is unloaded. 



#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms633575(v=VS.85).aspx">Using Window Classes</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632679(v=VS.85).aspx">CreateWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633499(v=VS.85).aspx">FindWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633500(v=VS.85).aspx">FindWindowEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633578(v=VS.85).aspx">GetClassInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633579(v=VS.85).aspx">GetClassInfoEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633582(v=VS.85).aspx">GetClassName</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644899(v=VS.85).aspx">UnregisterClass</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633577(v=VS.85).aspx">WNDCLASSEX</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632596(v=VS.85).aspx">Window Classes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633573(v=VS.85).aspx">WindowProc</a>
 

 

