---
UID: NF:winuser.GetPropA
title: GetPropA function
author: windows-sdk-content
description: Retrieves a data handle from the property list of the specified window. The character string identifies the handle to be retrieved. The string and handle must have been added to the property list by a previous call to the SetProp function.
old-location: winmsg\getprop.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\getprop.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetProp, GetProp function [Windows and Messages], GetPropA, GetPropW, _win32_GetProp, _win32_getprop_cpp, winmsg.getprop, winui._win32_getprop, winuser/GetProp, winuser/GetPropA, winuser/GetPropW
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
req.unicode-ansi: GetPropW (Unicode) and GetPropA (ANSI)
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetProp
 - GetPropA
 - GetPropW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPropA function


## -description


Retrieves a data handle from the property list of the specified window. The character string identifies the handle to be retrieved. The string and handle must have been added to the property list by a previous call to the <a href="https://msdn.microsoft.com/f447edbe-58a1-47e5-8efd-0acb10063ace">SetProp</a> function. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose property list is to be searched. 


### -param lpString [in]

Type: <b>LPCTSTR</b>

An atom that identifies a string. If this parameter is an atom, it must have been created by using the <a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a> function. The atom, a 16-bit value, must be placed in the low-order word of the <i>lpString</i> parameter; the high-order word must be zero. 


## -returns



Type: <strong>Type: <b>HANDLE</b>
</strong>

If the property list contains the string, the return value is the associated data handle. Otherwise, the return value is <b>NULL</b>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f447edbe-58a1-47e5-8efd-0acb10063ace">SetProp</a>



<a href="https://msdn.microsoft.com/c39902d3-5907-4aa9-b839-d2d67d273990">Window Properties</a>
 

 

