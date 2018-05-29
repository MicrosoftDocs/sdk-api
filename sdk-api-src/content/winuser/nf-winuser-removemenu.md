---
UID: NF:winuser.RemoveMenu
title: RemoveMenu function
author: windows-sdk-content
description: Deletes a menu item or detaches a submenu from the specified menu.
old-location: menurc\removemenu.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\removemenu.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: MF_BYCOMMAND, MF_BYPOSITION, RemoveMenu, RemoveMenu function [Menus and Other Resources], _win32_RemoveMenu, _win32_removemenu_cpp, menurc.removemenu, winui._win32_removemenu, winuser/RemoveMenu
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	Ext-MS-Win-NTUser-Menu-l1-1-0.dll
-	Ext-MS-Win-NTUser-Menu-l1-1-1.dll
-	ext-ms-win-ntuser-menu-l1-1-2.dll
-	Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
-	RemoveMenu
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RemoveMenu function


## -description


Deletes a menu item or detaches a submenu from the specified menu. If the menu item opens a drop-down menu or submenu, <b>RemoveMenu</b> does not destroy the menu or its handle, allowing the menu to be reused. Before this function is called, the <a href="https://msdn.microsoft.com/009ede3f-da6e-4195-90e0-9f046146fd5c">GetSubMenu</a> function should retrieve a handle to the drop-down menu or submenu. 


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
Indicates that <i>uPosition</i> gives the identifier of the menu item. If neither the <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> flag is specified, the <b>MF_BYCOMMAND</b> flag is the default flag.

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




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b1341fe7-1532-4e0b-82f3-540cc88c0aa7">CreatePopupMenu</a>



<a href="https://msdn.microsoft.com/0054bf62-cb70-4d6e-805d-58206fa2d297">DeleteMenu</a>



<a href="https://msdn.microsoft.com/3b17db02-5059-4182-bd5b-2fb67eecd1d7">DrawMenuBar</a>



<a href="https://msdn.microsoft.com/009ede3f-da6e-4195-90e0-9f046146fd5c">GetSubMenu</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

