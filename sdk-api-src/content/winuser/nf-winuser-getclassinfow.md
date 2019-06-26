---
UID: NF:winuser.GetClassInfoW
title: GetClassInfoW function (winuser.h)
author: windows-sdk-content
description: Retrieves information about a window class.
old-location: winmsg\getclassinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getclassinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetClassInfo, GetClassInfo function [Windows and Messages], GetClassInfoA, GetClassInfoW, _win32_GetClassInfo, _win32_getclassinfo_cpp, winmsg.getclassinfo, winui._win32_getclassinfo, winuser/GetClassInfo, winuser/GetClassInfoA, winuser/GetClassInfoW
ms.topic: function
f1_keywords: 
 - "winuser/GetClassInfo"
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
ms.custom: 19H1
---

# GetClassInfoW function


## -description


Retrieves information about a window class. 


			
<div class="alert"><b>Note</b>  The <b>GetClassInfo</b> function has been superseded by the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getclassinfoexa">GetClassInfoEx</a> function. You can still use <b>GetClassInfo</b>, however, if you do not need information about the class small icon.</div><div> </div>

## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the instance of the application that created the class. To retrieve information about classes defined by the system (such as buttons or list boxes), set this parameter to <b>NULL</b>. 


### -param lpClassName [in]

Type: <b>LPCTSTR</b>

The class name. The name must be that of a preregistered class or a class registered by a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. 

Alternatively, this parameter can be an atom. If so, it must be a class atom created by a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>. The atom must be in the low-order word of 
					<i>lpClassName</i>; the high-order word must be zero.


### -param lpWndClass [out]

Type: <b>LPWNDCLASS</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-tagwndclassa">WNDCLASS</a> structure that receives the information about the class. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function finds a matching class and successfully copies the data, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getclassinfoexa">GetClassInfoEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getclasslonga">GetClassLong</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getclassname">GetClassName</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-tagwndclassa">WNDCLASS</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/window-classes">Window Classes</a>
 

 

