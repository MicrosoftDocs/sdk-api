---
UID: NC:winuser.PROPENUMPROCEXA
title: PROPENUMPROCEXA
author: windows-sdk-content
description: Application-defined callback function used with the EnumPropsEx function.
old-location: winmsg\propenumprocex.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\propenumprocex.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PropEnumProcEx, PropEnumProcEx callback, PropEnumProcEx callback function [Windows and Messages], PropEnumProcExA, PropEnumProcExW, _win32_PropEnumProcEx, _win32_propenumprocex_cpp, winmsg.propenumprocex, winui._win32_propenumprocex, winuser/PropEnumProcEx, winuser/PropEnumProcExA, winuser/PropEnumProcExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
 - PropEnumProcEx
 - PropEnumProcExA
 - PropEnumProcExW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# PROPENUMPROCEXA callback function


## -description


Application-defined callback function used with the <a href="https://msdn.microsoft.com/a23e75be-f403-481e-ad5a-c8c59b632416">EnumPropsEx</a> function. The function receives property entries from a window's property list. The PROPENUMPROCEX type defines a pointer to this callback function. <b>PropEnumProcEx</b> is a placeholder for the application-defined function name. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - dwData [in]

Type: <b>ULONG_PTR</b>

Application-defined data. This is the value that was specified as the <i>lParam</i> parameter of the call to <a href="https://msdn.microsoft.com/a23e75be-f403-481e-ad5a-c8c59b632416">EnumPropsEx</a> that initiated the enumeration. 


#### - hData [in]

Type: <b>HANDLE</b>

A  handle to the data. This handle is the data component of a property list entry. 


#### - hwnd [in]

Type: <b>HWND</b>

A handle to the window whose property list is being enumerated. 


#### - lpszString [in]

Type: <b>LPTSTR</b>

The string component of a property list entry. This is the string that was specified, along with a data handle, when the property was added to the window's property list via a call to the <a href="https://msdn.microsoft.com/f447edbe-58a1-47e5-8efd-0acb10063ace">SetProp</a> function. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

Return <b>TRUE</b> to continue the property list enumeration.

Return <b>FALSE</b> to stop the property list enumeration. 




## -remarks



The following restrictions apply to this callback function: 

<ul>
<li>The callback function can call the <a href="https://msdn.microsoft.com/02852980-a2fd-47c6-82f3-fccc135e8fb2">RemoveProp</a> function. However, <b>RemoveProp</b> can remove only the property passed to the callback function through the callback function's parameters. </li>
<li>The callback function should not attempt to add properties. </li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a23e75be-f403-481e-ad5a-c8c59b632416">EnumPropsEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/02852980-a2fd-47c6-82f3-fccc135e8fb2">RemoveProp</a>



<a href="https://msdn.microsoft.com/f447edbe-58a1-47e5-8efd-0acb10063ace">SetProp</a>



<a href="https://msdn.microsoft.com/c39902d3-5907-4aa9-b839-d2d67d273990">Window Properties</a>
 

 

