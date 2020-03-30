---
UID: NC:winuser.PROPENUMPROCEXW
title: PROPENUMPROCEXW (winuser.h)
description: Application-defined callback function used with the EnumPropsEx function.
old-location: winmsg\propenumprocex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\propenumprocex.htm
ms.date: 12/05/2018
ms.keywords: PropEnumProcEx, PropEnumProcEx callback, PropEnumProcEx callback function [Windows and Messages], PropEnumProcExA, PropEnumProcExW, _win32_PropEnumProcEx, _win32_propenumprocex_cpp, winmsg.propenumprocex, winui._win32_propenumprocex, winuser/PropEnumProcEx, winuser/PropEnumProcExA, winuser/PropEnumProcExW
f1_keywords:
- winuser/PropEnumProcEx
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
req.unicode-ansi: PropEnumProcExW (Unicode) and PropEnumProcExA (ANSI)
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
- PropEnumProcEx
- PropEnumProcExA
- PropEnumProcExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PROPENUMPROCEXW callback function


## -description


Application-defined callback function used with the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumpropsexa">EnumPropsEx</a> function. The function receives property entries from a window's property list. The PROPENUMPROCEX type defines a pointer to this callback function. <b>PropEnumProcEx</b> is a placeholder for the application-defined function name. 


## -parameters




### -param Arg1

Type: <b>HWND</b>

A handle to the window whose property list is being enumerated. 


### -param Arg2

Type: <b>LPTSTR</b>

The string component of a property list entry. This is the string that was specified, along with a data handle, when the property was added to the window's property list via a call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setpropa">SetProp</a> function. 


### -param Arg3

Type: <b>HANDLE</b>

A  handle to the data. This handle is the data component of a property list entry. 

### -param Arg4

Type: <b>ULONG_PTR</b>

Application-defined data. This is the value that was specified as the <i>lParam</i> parameter of the call to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumpropsexa">EnumPropsEx</a> that initiated the enumeration. 



## -returns



Type: <b>BOOL</b>

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



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-enumpropsexa">EnumPropsEx</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-removepropa">RemoveProp</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setpropa">SetProp</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/window-properties">Window Properties</a>
 

 

