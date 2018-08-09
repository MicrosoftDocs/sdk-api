---
UID: NF:winuser.EnumPropsExW
title: EnumPropsExW function
author: windows-sdk-content
description: Enumerates all entries in the property list of a window by passing them, one by one, to the specified callback function. EnumPropsEx continues until the last entry is enumerated or the callback function returns FALSE.
old-location: winmsg\enumpropsex.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\enumpropsex.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EnumPropsEx, EnumPropsEx function [Windows and Messages], EnumPropsExA, EnumPropsExW, _win32_EnumPropsEx, _win32_enumpropsex_cpp, winmsg.enumpropsex, winui._win32_enumpropsex, winuser/EnumPropsEx, winuser/EnumPropsExA, winuser/EnumPropsExW
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
req.unicode-ansi: EnumPropsExW (Unicode) and EnumPropsExA (ANSI)
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
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - EnumPropsEx
 - EnumPropsExA
 - EnumPropsExW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumPropsExW function


## -description


Enumerates all entries in the property list of a window by passing them, one by one, to the specified callback function. <b>EnumPropsEx</b> continues until the last entry is enumerated or the callback function returns <b>FALSE</b>. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose property list is to be enumerated. 


### -param lpEnumFunc [in]

Type: <b>PROPENUMPROCEX</b>

A pointer to the callback function. For more information about the callback function, see the <a href="https://msdn.microsoft.com/en-us/library/ms633566(v=VS.85).aspx">PropEnumProcEx</a> function. 


### -param lParam [in]

Type: <b>LPARAM</b>

Application-defined data to be passed to the callback function. 


## -returns



Type: <strong>Type: <b>int</b>
</strong>

The return value specifies the last value returned by the callback function. It is -1 if the function did not find a property for enumeration. 




## -remarks



An application can remove only those properties it has added. It must not remove properties added by other applications or by the system itself. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms633561(v=VS.85).aspx">Listing Window Properties for a Given Window</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633566(v=VS.85).aspx">PropEnumProcEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632594(v=VS.85).aspx">Window Properties</a>
 

 

