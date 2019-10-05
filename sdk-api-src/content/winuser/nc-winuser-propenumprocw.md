---
UID: NC:winuser.PROPENUMPROCW
title: PROPENUMPROCW (winuser.h)
author: windows-sdk-content
description: An application-defined callback function used with the EnumProps function.
old-location: winmsg\propenumproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\propenumproc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropEnumProc, PropEnumProc callback, PropEnumProc callback function [Windows and Messages], PropEnumProcA, PropEnumProcW, _win32_PropEnumProc, _win32_propenumproc_cpp, winmsg.propenumproc, winui._win32_propenumproc, winuser/PropEnumProc, winuser/PropEnumProcA, winuser/PropEnumProcW
ms.topic: callback
f1_keywords: 
 - "winuser/PropEnumProc"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PROPENUMPROCW callback function


## -description


An application-defined callback function used with the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumpropsa">EnumProps</a> function. The function receives property entries from a window's property list. The <b>PROPENUMPROC</b> type defines a pointer to this callback function. <i>PropEnumProc</i> is a placeholder for the application-defined function name. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - hData [in]

Type: <b>HANDLE</b>

A handle to the data. This handle is the data component of a property list entry. 


#### - hwnd [in]

Type: <b>HWND</b>

A handle to the window whose property list is being enumerated. 


#### - lpszString [in]

Type: <b>LPCTSTR</b>

The string component of a property list entry. This is the string that was specified, along with a data handle, when the property was added to the window's property list via a call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setpropa">SetProp</a> function. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

Return <b>TRUE</b> to continue the property list enumeration.

Return <b>FALSE</b> to stop the property list enumeration. 




## -remarks



The following restrictions apply to this callback function: 

<ul>
<li>The callback function can call the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-removepropa">RemoveProp</a> function. However, <b>RemoveProp</b> can remove only the property passed to the callback function through the callback function's parameters. </li>
<li>The callback function should not attempt to add properties. </li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumpropsa">EnumProps</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-removepropa">RemoveProp</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setpropa">SetProp</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/window-properties">Window Properties</a>
 

 

