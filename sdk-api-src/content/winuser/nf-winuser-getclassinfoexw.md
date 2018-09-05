---
UID: NF:winuser.GetClassInfoExW
title: GetClassInfoExW function
author: windows-sdk-content
description: Retrieves information about a window class, including a handle to the small icon associated with the window class. The GetClassInfo function does not retrieve a handle to the small icon.
old-location: winmsg\getclassinfoex.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getclassinfoex.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetClassInfoEx, GetClassInfoEx function [Windows and Messages], GetClassInfoExA, GetClassInfoExW, _win32_GetClassInfoEx, _win32_getclassinfoex_cpp, winmsg.getclassinfoex, winui._win32_getclassinfoex, winuser/GetClassInfoEx, winuser/GetClassInfoExA, winuser/GetClassInfoExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetClassInfoExW (Unicode) and GetClassInfoExA (ANSI)
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
 - GetClassInfoEx
 - GetClassInfoExA
 - GetClassInfoExW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetClassInfoExW function


## -description


Retrieves information about a window class, including a handle to the small icon associated with the window class. The <a href="https://msdn.microsoft.com/f7eb12c9-ff24-465d-8c6d-8ee5777c05bc">GetClassInfo</a> function does not retrieve a handle to the small icon.


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the instance of the application that created the class. To retrieve information about classes defined by the system (such as buttons or list boxes), set this parameter to <b>NULL</b>. 


### -param lpszClass [in]

Type: <b>LPCTSTR</b>

The class name. The name must be that of a preregistered class or a class registered by a previous call to the <a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a> or <a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a> function. Alternatively, this parameter can be a class atom created by a previous call to <b>RegisterClass</b> or <b>RegisterClassEx</b>. The atom must be in the low-order word of 
					<i>lpszClass</i>; the high-order word must be zero. 


### -param lpwcx [out]

Type: <b>LPWNDCLASSEX</b>

A pointer to a <a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a> structure that receives the information about the class. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function finds a matching class and successfully copies the data, the return value is nonzero.

If the function does not find a matching class and successfully copy the data, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Class atoms are created using the <a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a> or <a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a> function, not the 
				<a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8d8e0b2e-635f-4612-8279-a07679c9a144">GetClassLong</a>



<a href="https://msdn.microsoft.com/039dd7cd-07cf-4c8a-9287-365d54da2f43">GetClassName</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a>



<a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/6ef633db-af76-42d6-b211-96846578eaac">Window Classes</a>
 

 

