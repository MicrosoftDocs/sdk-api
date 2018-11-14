---
UID: NF:winuser.EnumPropsW
title: EnumPropsW function
author: windows-sdk-content
description: Enumerates all entries in the property list of a window by passing them, one by one, to the specified callback function. EnumProps continues until the last entry is enumerated or the callback function returns FALSE.
old-location: winmsg\enumprops.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\enumprops.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: EnumProps, EnumProps function [Windows and Messages], EnumPropsA, EnumPropsW, _win32_EnumProps, _win32_enumprops_cpp, winmsg.enumprops, winui._win32_enumprops, winuser/EnumProps, winuser/EnumPropsA, winuser/EnumPropsW
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
req.unicode-ansi: EnumPropsW (Unicode) and EnumPropsA (ANSI)
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
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - EnumProps
 - EnumPropsA
 - EnumPropsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EnumPropsW
: 
---

# EnumPropsW function


## -description


Enumerates all entries in the property list of a window by passing them, one by one, to the specified callback function. <b>EnumProps</b> continues until the last entry is enumerated or the callback function returns <b>FALSE</b>.

To pass application-defined data to the callback function, use <a href="https://msdn.microsoft.com/en-us/library/ms633563(v=VS.85).aspx">EnumPropsEx</a> function.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose property list is to be enumerated. 


### -param lpEnumFunc [in]

Type: <b>PROPENUMPROC</b>

A pointer to the callback function. For more information about the callback function, see the <a href="https://msdn.microsoft.com/en-us/library/ms633565(v=VS.85).aspx">PropEnumProc</a> function. 


## -returns



Type: <strong>Type: <b>int</b>
</strong>

The return value specifies the last value returned by the callback function. It is -1 if the function did not find a property for enumeration. 




## -remarks



An application can remove only those properties it has added. It must not remove properties added by other applications or by the system itself. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633563(v=VS.85).aspx">EnumPropsEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633565(v=VS.85).aspx">PropEnumProc</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632594(v=VS.85).aspx">Window Properties</a>
 

 

