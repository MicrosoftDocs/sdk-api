---
UID: NF:winuser.GetClassInfoW
title: GetClassInfoW function
author: windows-sdk-content
description: Retrieves information about a window class.
old-location: winmsg\getclassinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getclassinfo.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetClassInfo, GetClassInfo function [Windows and Messages], GetClassInfoA, GetClassInfoW, _win32_GetClassInfo, _win32_getclassinfo_cpp, winmsg.getclassinfo, winui._win32_getclassinfo, winuser/GetClassInfo, winuser/GetClassInfoA, winuser/GetClassInfoW
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
req.unicode-ansi: GetClassInfoW (Unicode) and GetClassInfoA (ANSI)
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
 - GetClassInfo
 - GetClassInfoA
 - GetClassInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClassInfoW function


## -description


Retrieves information about a window class. 


			
<div class="alert"><b>Note</b>  The <b>GetClassInfo</b> function has been superseded by the <a href="https://msdn.microsoft.com/a353eaa2-7a79-4008-84fe-a72847350745">GetClassInfoEx</a> function. You can still use <b>GetClassInfo</b>, however, if you do not need information about the class small icon.</div><div> </div>

## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the instance of the application that created the class. To retrieve information about classes defined by the system (such as buttons or list boxes), set this parameter to <b>NULL</b>. 


### -param lpClassName [in]

Type: <b>LPCTSTR</b>

The class name. The name must be that of a preregistered class or a class registered by a previous call to the <a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a> or <a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a> function. 

Alternatively, this parameter can be an atom. If so, it must be a class atom created by a previous call to <a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a> or <a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a>. The atom must be in the low-order word of 
					<i>lpClassName</i>; the high-order word must be zero.


### -param lpWndClass [out]

Type: <b>LPWNDCLASS</b>

A pointer to a <a href="https://msdn.microsoft.com/7e2a4e89-19b6-4ef7-81dd-f44a3874e546">WNDCLASS</a> structure that receives the information about the class. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function finds a matching class and successfully copies the data, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a353eaa2-7a79-4008-84fe-a72847350745">GetClassInfoEx</a>



<a href="https://msdn.microsoft.com/8d8e0b2e-635f-4612-8279-a07679c9a144">GetClassLong</a>



<a href="https://msdn.microsoft.com/039dd7cd-07cf-4c8a-9287-365d54da2f43">GetClassName</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a>



<a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/7e2a4e89-19b6-4ef7-81dd-f44a3874e546">WNDCLASS</a>



<a href="https://msdn.microsoft.com/6ef633db-af76-42d6-b211-96846578eaac">Window Classes</a>
 

 

