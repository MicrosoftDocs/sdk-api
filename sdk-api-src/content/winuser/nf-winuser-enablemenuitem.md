---
UID: NF:winuser.EnableMenuItem
title: EnableMenuItem function
author: windows-sdk-content
description: Enables, disables, or grays the specified menu item.
old-location: menurc\enablemenuitem.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\enablemenuitem.htm
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: EnableMenuItem, EnableMenuItem function [Menus and Other Resources], MF_BYCOMMAND, MF_BYPOSITION, MF_DISABLED, MF_ENABLED, MF_GRAYED, _win32_EnableMenuItem, _win32_enablemenuitem_cpp, menurc.enablemenuitem, winui._win32_enablemenuitem, winuser/EnableMenuItem
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
tech.root: 
req.typenames: 
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
 - EnableMenuItem
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnableMenuItem function


## -description


Enables, disables, or grays the specified menu item. 


## -parameters




### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu. 


### -param uIDEnableItem [in]

Type: <b>UINT</b>

The menu item to be enabled, disabled, or grayed, as determined by the <i>uEnable</i> parameter. This parameter specifies an item in a menu bar, menu, or submenu. 


### -param uEnable [in]

Type: <b>UINT</b>

Controls the interpretation of the <i>uIDEnableItem</i> parameter and indicate whether the menu item is enabled, disabled, or grayed. This parameter must be a combination of the following values. 

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
Indicates that <i>uIDEnableItem</i> gives the identifier of the menu item. If neither the <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> flag is specified, the <b>MF_BYCOMMAND</b> flag is the default flag.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uIDEnableItem</i> gives the zero-based relative position of the menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_DISABLED"></a><a id="mf_disabled"></a><dl>
<dt><b>MF_DISABLED</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is disabled, but not grayed, so it cannot be selected.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_ENABLED"></a><a id="mf_enabled"></a><dl>
<dt><b>MF_ENABLED</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is enabled and restored from a grayed state so that it can be selected.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_GRAYED"></a><a id="mf_grayed"></a><dl>
<dt><b>MF_GRAYED</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is disabled and grayed so that it cannot be selected.

</td>
</tr>
</table>
 


## -returns



Type: <b>BOOL</b>

The return value specifies the previous state of the menu item (it is either <b>MF_DISABLED</b>, <b>MF_ENABLED</b>, or <b>MF_GRAYED</b>). If the menu item does not exist, the return value is -1.




## -remarks



An application must use the <b>MF_BYPOSITION</b> flag to specify the correct menu handle. If the menu handle to the menu bar is specified, the top-level menu item (an item in the menu bar) is affected. To set the state of an item in a drop-down menu or submenu by position, an application must specify a handle to the drop-down menu or submenu. 

When an application specifies the <b>MF_BYCOMMAND</b> flag, the system checks all items that open submenus in the menu identified by the specified menu handle. Therefore, unless duplicate menu items are present, specifying the menu handle to the menu bar is sufficient. 

The <a href="https://msdn.microsoft.com/8ca7510a-e035-4ba2-98dd-57d777cae814">InsertMenu</a>, <a href="https://msdn.microsoft.com/be3819c2-8bdc-4a90-a188-ff8b4060eb8f">InsertMenuItem</a>, <a href="https://msdn.microsoft.com/01736486-6dee-43fe-80a7-06c4cf13a23e">LoadMenuIndirect</a>, <a href="https://msdn.microsoft.com/2e6abd30-9ace-4a17-9cf6-8a45a71eecaf">ModifyMenu</a>, and <a href="https://msdn.microsoft.com/e1c669c7-7b56-428a-8433-d926330e42e1">SetMenuItemInfo</a> functions can also set the state (enabled, disabled, or grayed) of a menu item.

When you change a window menu, the menu bar is not immediately updated. To force the update, call <a href="https://msdn.microsoft.com/3b17db02-5059-4182-bd5b-2fb67eecd1d7">DrawMenuBar</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/3b17db02-5059-4182-bd5b-2fb67eecd1d7">DrawMenuBar</a>



<a href="https://msdn.microsoft.com/69ecdcba-177c-4465-95ae-897ed4e96c2d">GetMenuItemID</a>



<a href="https://msdn.microsoft.com/8ca7510a-e035-4ba2-98dd-57d777cae814">InsertMenu</a>



<a href="https://msdn.microsoft.com/be3819c2-8bdc-4a90-a188-ff8b4060eb8f">InsertMenuItem</a>



<a href="https://msdn.microsoft.com/01736486-6dee-43fe-80a7-06c4cf13a23e">LoadMenuIndirect</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<a href="https://msdn.microsoft.com/2e6abd30-9ace-4a17-9cf6-8a45a71eecaf">ModifyMenu</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e1c669c7-7b56-428a-8433-d926330e42e1">SetMenuItemInfo</a>



<a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a>
 

 

