---
UID: NF:winuser.RemovePropA
title: RemovePropA function (winuser.h)
author: windows-sdk-content
description: Removes an entry from the property list of the specified window. The specified character string identifies the entry to be removed.
old-location: winmsg\removeprop.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\removeprop.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RemoveProp, RemoveProp function [Windows and Messages], RemovePropA, RemovePropW, _win32_RemoveProp, _win32_removeprop_cpp, winmsg.removeprop, winui._win32_removeprop, winuser/RemoveProp, winuser/RemovePropA, winuser/RemovePropW
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemovePropW (Unicode) and RemovePropA (ANSI)
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - RemoveProp
 - RemovePropA
 - RemovePropW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RemovePropA function


## -description


Removes an entry from the property list of the specified window. The specified character string identifies the entry to be removed.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose property list is to be changed.


### -param lpString [in]

Type: <b>LPCTSTR</b>

A null-terminated character string or an atom that identifies a string. If this parameter is an atom, it must have been created using the <a href="https://msdn.microsoft.com/en-us/library/ms649060(v=VS.85).aspx">GlobalAddAtom</a> function. The atom, a 16-bit value, must be placed in the low-order word of <i>lpString</i>; the high-order word must be zero.


## -returns



Type: <strong>Type: <b>HANDLE</b>
</strong>

The return value identifies the specified data. If the data cannot be found in the specified property list, the return value is <b>NULL</b>.




## -remarks



The return value is the <i>hData</i> value that was passed to <a href="https://msdn.microsoft.com/en-us/library/ms633568(v=VS.85).aspx">SetProp</a>; it is an application-defined value. Note, this function only destroys the association between the data and the window. If appropriate, the application must free the data handles associated with entries removed from a property list. The application can remove only those properties it has added. It must not remove properties added by other applications or by the system itself.

The <b>RemoveProp</b> function returns the data handle associated with the string so that the application can free the data associated with the handle.

Starting with Windows Vista, <b>RemoveProp</b> is subject to the restrictions of User Interface Privilege Isolation (UIPI). A process can only call this function on a window belonging to a process of lesser or equal integrity level. When UIPI blocks property changes, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return <b>5</b>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms633561(v=VS.85).aspx">Deleting a Window Property</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649056(v=VS.85).aspx">AddAtom</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633564(v=VS.85).aspx">GetProp</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633568(v=VS.85).aspx">SetProp</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632594(v=VS.85).aspx">Window Properties</a>
 

 

