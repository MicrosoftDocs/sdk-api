---
UID: NF:shlobj_core.Shell_MergeMenus
title: Shell_MergeMenus function
author: windows-sdk-content
description: Shell_MergeMenus may be altered or unavailable.
old-location: shell\Shell_MergeMenus.htm
tech.root: shell
ms.assetid: f9e005fd-b1f2-4a5f-ad36-9c44998dc4eb
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: MM_ADDSEPARATOR, MM_DONTREMOVESEPS, MM_SUBMENUSHAVEIDS, Shell_MergeMenus, Shell_MergeMenus function [Windows Shell], _win32_Shell_MergeMenus, shell.Shell_MergeMenus, shlobj_core/Shell_MergeMenus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - Shell_MergeMenus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Shell_MergeMenus function


## -description


<p class="CCE_Message">[<b>Shell_MergeMenus</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Merges two menus.


## -parameters




### -param hmDst [in]

Type: <b>HMENU</b>

The destination menu to which <i>hmSrc</i> is added.


### -param hmSrc [in]

Type: <b>HMENU</b>

The source menu which is added to <i>hmDst</i>.


### -param uInsert

Type: <b>UINT</b>

The point in <i>hmDst</i> after which the entries in <i>hmSrc</i> are inserted.


### -param uIDAdjust

Type: <b>UINT</b>

This number is added to each menu's ID to give an adjusted ID. Set to <code>0</code> for no adjustment. The value for <i>uIDAdjust</i> would typically be the number of items in <i>hmDst</i>. This number can be obtained using the <a href="https://msdn.microsoft.com/en-us/library/ms647978(v=VS.85).aspx">GetMenuItemCount</a>.


### -param uIDAdjustMax

Type: <b>UINT</b>

The maximum adjusted ID to add to the menu. Any adjusted ID greater than this value is not added. To allow all IDs, set this parameter to 0xFFFF.


### -param uFlags

Type: <b>ULONG</b>

One or more of the following flags.



#### MM_ADDSEPARATOR

Add a separator between the items from the two menus if one does not exist already. If you are inserting the entries from <i>hmSrc</i> into the middle of <i>hmDst</i>, a separator is added above and below the <i>hmSrc</i> material.



#### MM_DONTREMOVESEPS

Do not remove any existing separators in the two menus. Note that this could result in two separators in a row.



#### MM_SUBMENUSHAVEIDS

Set this flag if the submenus have IDs which should be adjusted.


## -returns



Type: <b>UINT</b>

Returns the next open ID at the end of the menu (the maximum adjusted ID + 1).



