---
UID: NC:winuser.PROPENUMPROCA
title: PROPENUMPROCA
author: windows-sdk-content
description: An application-defined callback function used with the EnumProps function.
old-location: winmsg\propenumproc.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\propenumproc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropEnumProc, PropEnumProc callback, PropEnumProc callback function [Windows and Messages], PropEnumProcA, PropEnumProcW, _win32_PropEnumProc, _win32_propenumproc_cpp, winmsg.propenumproc, winui._win32_propenumproc, winuser/PropEnumProc, winuser/PropEnumProcA, winuser/PropEnumProcW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PropEnumProcW (Unicode) and PropEnumProcA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WINUSB_PIPE_INFORMATION_EX, *PWINUSB_PIPE_INFORMATION_EX
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - PropEnumProc
 - PropEnumProcA
 - PropEnumProcW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# PROPENUMPROCA callback function


## -description


An application-defined callback function used with the <a href="https://msdn.microsoft.com/en-us/library/ms633562(v=VS.85).aspx">EnumProps</a> function. The function receives property entries from a window's property list. The <b>PROPENUMPROC</b> type defines a pointer to this callback function. <i>PropEnumProc</i> is a placeholder for the application-defined function name. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - hwnd [in]

Type: <b>HWND</b>

A handle to the window whose property list is being enumerated. 


#### - lpszString [in]

Type: <b>LPCTSTR</b>

The string component of a property list entry. This is the string that was specified, along with a data handle, when the property was added to the window's property list via a call to the <a href="https://msdn.microsoft.com/en-us/library/ms633568(v=VS.85).aspx">SetProp</a> function. 


#### - hData [in]

Type: <b>HANDLE</b>

A handle to the data. This handle is the data component of a property list entry. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

Return <b>TRUE</b> to continue the property list enumeration.

Return <b>FALSE</b> to stop the property list enumeration. 




## -remarks



The following restrictions apply to this callback function: 

<ul>
<li>The callback function can call the <a href="https://msdn.microsoft.com/en-us/library/ms633567(v=VS.85).aspx">RemoveProp</a> function. However, <b>RemoveProp</b> can remove only the property passed to the callback function through the callback function's parameters. </li>
<li>The callback function should not attempt to add properties. </li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633562(v=VS.85).aspx">EnumProps</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633567(v=VS.85).aspx">RemoveProp</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633568(v=VS.85).aspx">SetProp</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632594(v=VS.85).aspx">Window Properties</a>
 

 

