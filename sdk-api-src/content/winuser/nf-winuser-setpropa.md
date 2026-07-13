---
UID: NF:winuser.SetPropA
title: SetPropA function (winuser.h)
description: Adds a new entry or changes an existing entry in the property list of the specified window. (ANSI)
helpviewer_keywords: ["SetPropA", "winuser/SetPropA"]
old-location: winmsg\setprop.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\setprop.htm
ms.date: 12/05/2018
ms.keywords: SetProp, SetProp function [Windows and Messages], SetPropA, SetPropW, _win32_SetProp, _win32_setprop_cpp, winmsg.setprop, winui._win32_setprop, winuser/SetProp, winuser/SetPropA, winuser/SetPropW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetPropW (Unicode) and SetPropA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetPropA
 - winuser/SetPropA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
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
 - SetProp
 - SetPropA
 - SetPropW
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# SetPropA function


## -description

Adds a new entry or changes an existing entry in the property list of the specified window. The function adds a new entry to the list if the specified character string does not exist already in the list. The new entry contains the string and the handle. Otherwise, the function replaces the string's current handle with the specified handle.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose property list receives the new entry.

### -param lpString [in]

Type: <b>LPCTSTR</b>

A null-terminated string or an atom that identifies a string. If this parameter is an atom, it must be a global atom created by a previous call to the <a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a> function. The atom must be placed in the low-order word of <i>lpString</i>; the high-order word must be zero.

### -param hData [in, optional]

Type: <b>HANDLE</b>

A handle to the data to be copied to the property list. The data handle can identify any value useful to the application.

## -returns

Type: <b>BOOL</b>

If the data handle and string are added to the property list, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Before a window is destroyed (that is, before it returns from processing the <a href="/windows/desktop/winmsg/wm-ncdestroy">WM_NCDESTROY</a> message), an application must remove all entries it has added to the property list. The application must use the <a href="/windows/desktop/api/winuser/nf-winuser-removepropa">RemoveProp</a> function to remove the entries. 

<b>SetProp</b> is subject to the restrictions of User Interface Privilege Isolation (UIPI). A process can only call this function on a window belonging to a process of lesser or equal integrity level. When UIPI blocks property changes, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 5.


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-window-properties">Adding a Window Property</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines SetProp as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-removepropa">RemoveProp</a>



<a href="/windows/desktop/winmsg/wm-ncdestroy">WM_NCDESTROY</a>



<a href="/windows/desktop/winmsg/window-properties">Window Properties</a>



<a href="/windows/win32/api/shobjidl_core/nf-shobjidl_core-itaskbarlist2-markfullscreenwindow">ITaskbarList2::MarkFullscreenWindow</a>
