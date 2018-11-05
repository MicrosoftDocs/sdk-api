---
UID: NF:winuser.DeleteMenu
title: DeleteMenu function
author: windows-sdk-content
description: Deletes an item from the specified menu. If the menu item opens a menu or submenu, this function destroys the handle to the menu or submenu and frees the memory used by the menu or submenu.
old-location: menurc\deletemenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\deletemenu.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DeleteMenu, DeleteMenu function [Menus and Other Resources], MF_BYCOMMAND, MF_BYPOSITION, _win32_DeleteMenu, _win32_deletemenu_cpp, menurc.deletemenu, winui._win32_deletemenu, winuser/DeleteMenu
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
 - Ext-MS-Win-NTUser-Menu-l1-1-0.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - DeleteMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteMenu function


## -description


Deletes an item from the specified menu. If the menu item opens a menu or submenu, this function destroys the handle to the menu or submenu and frees the memory used by the menu or submenu. 


## -parameters




### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu to be changed. 


### -param uPosition [in]

Type: <b>UINT</b>

The menu item to be deleted, as determined by the <i>uFlags</i> parameter. 


### -param uFlags [in]

Type: <b>UINT</b>

Indicates how the <i>uPosition</i> parameter is interpreted. This parameter must be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_BYCOMMAND"></a><a id="mf_bycommand"></a><dl>
<dt><b>MF_BYCOMMAND</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uPosition</i> gives the identifier of the menu item. The <b>MF_BYCOMMAND</b> flag is the default flag if neither the <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> flag is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uPosition</i> gives the zero-based relative position of the menu item.

</td>
</tr>
</table>
 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The application must call the <a href="https://msdn.microsoft.com/3b17db02-5059-4182-bd5b-2fb67eecd1d7">DrawMenuBar</a> function whenever a menu changes, whether the menu is in a displayed window. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/377fb2cc-5b46-481a-8222-9291e504ae2c">Example of a Clipboard Viewer</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3b17db02-5059-4182-bd5b-2fb67eecd1d7">DrawMenuBar</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9557d6dd-44a2-4c26-b939-8ae88b48956a">RemoveMenu</a>
 

 

