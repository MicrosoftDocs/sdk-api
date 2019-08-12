---
UID: NF:winuser.GetMenuBarInfo
title: GetMenuBarInfo function (winuser.h)
author: windows-sdk-content
description: Retrieves information about the specified menu bar.
old-location: menurc\getmenubarinfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenubarinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMenuBarInfo, GetMenuBarInfo function [Menus and Other Resources], OBJID_CLIENT, OBJID_MENU, OBJID_SYSMENU, _win32_GetMenuBarInfo, _win32_getmenubarinfo_cpp, menurc.getmenubarinfo, winui._win32_getmenubarinfo, winuser/GetMenuBarInfo
ms.topic: function
f1_keywords: 
 - "winuser/GetMenuBarInfo"
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - Ext-MS-Win-NTUser-Misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetMenuBarInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMenuBarInfo function


## -description


Retrieves information about the specified menu bar.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window (menu bar) whose information is to be retrieved. 


### -param idObject [in]

Type: <b>LONG</b>

The menu object. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OBJID_CLIENT"></a><a id="objid_client"></a><dl>
<dt><b>OBJID_CLIENT</b></dt>
<dt>((LONG)0xFFFFFFFC)</dt>
</dl>
</td>
<td width="60%">
The popup menu associated with the window.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJID_MENU"></a><a id="objid_menu"></a><dl>
<dt><b>OBJID_MENU</b></dt>
<dt>((LONG)0xFFFFFFFD)</dt>
</dl>
</td>
<td width="60%">
The menu bar associated with the window (see the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getmenu">GetMenu</a> function).

</td>
</tr>
<tr>
<td width="40%"><a id="OBJID_SYSMENU"></a><a id="objid_sysmenu"></a><dl>
<dt><b>OBJID_SYSMENU</b></dt>
<dt>((LONG)0xFFFFFFFF)</dt>
</dl>
</td>
<td width="60%">
The system menu associated with the window (see the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getsystemmenu">GetSystemMenu</a> function).

</td>
</tr>
</table>
 


### -param idItem [in]

Type: <b>LONG</b>

The item for which to retrieve information. If this parameter is zero, the function retrieves information about the menu itself. If this parameter is 1, the function retrieves information about the first item on the menu, and so on. 


### -param pmbi [in, out]

Type: <b>PMENUBARINFO</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-menubarinfo">MENUBARINFO</a> structure that receives the information. Note that you must set the <b>cbSize</b> member to <code>sizeof(MENUBARINFO)</code> before calling this function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getmenu">GetMenu</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getsystemmenu">GetSystemMenu</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-menubarinfo">MENUBARINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
 

 

