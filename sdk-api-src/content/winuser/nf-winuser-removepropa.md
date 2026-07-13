---
UID: NF:winuser.RemovePropA
title: RemovePropA function (winuser.h)
description: Removes an entry from the property list of the specified window. The specified character string identifies the entry to be removed. (ANSI)
helpviewer_keywords: ["RemovePropA", "winuser/RemovePropA"]
old-location: winmsg\removeprop.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowproperties\windowpropertyreference\windowpropertyfunctions\removeprop.htm
ms.date: 12/05/2018
ms.keywords: RemoveProp, RemoveProp function [Windows and Messages], RemovePropA, RemovePropW, _win32_RemoveProp, _win32_removeprop_cpp, winmsg.removeprop, winui._win32_removeprop, winuser/RemoveProp, winuser/RemovePropA, winuser/RemovePropW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RemovePropA
 - winuser/RemovePropA
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
 - RemoveProp
 - RemovePropA
 - RemovePropW
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
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

A null-terminated character string or an atom that identifies a string. If this parameter is an atom, it must have been created using the <a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a> function. The atom, a 16-bit value, must be placed in the low-order word of <i>lpString</i>; the high-order word must be zero.

## -returns

Type: <b>HANDLE</b>

The return value identifies the specified data. If the data cannot be found in the specified property list, the return value is <b>NULL</b>.

## -remarks

The return value is the <i>hData</i> value that was passed to <a href="/windows/desktop/api/winuser/nf-winuser-setpropa">SetProp</a>; it is an application-defined value. Note, this function only destroys the association between the data and the window. If appropriate, the application must free the data handles associated with entries removed from a property list. The application can remove only those properties it has added. It must not remove properties added by other applications or by the system itself.

The <b>RemoveProp</b> function returns the data handle associated with the string so that the application can free the data associated with the handle.

Starting with Windows Vista, <b>RemoveProp</b> is subject to the restrictions of User Interface Privilege Isolation (UIPI). A process can only call this function on a window belonging to a process of lesser or equal integrity level. When UIPI blocks property changes, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return <b>5</b>.


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-window-properties">Deleting a Window Property</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines RemoveProp as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-addatomw">AddAtom</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getpropa">GetProp</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setpropa">SetProp</a>



<a href="/windows/desktop/winmsg/window-properties">Window Properties</a>
