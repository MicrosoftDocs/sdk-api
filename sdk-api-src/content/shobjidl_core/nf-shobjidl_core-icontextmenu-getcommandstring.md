---
UID: NF:shobjidl_core.IContextMenu.GetCommandString
title: IContextMenu::GetCommandString (shobjidl_core.h)
description: Gets information about a shortcut menu command, including the help string and the language-independent, or canonical, name for the command.
helpviewer_keywords: ["GCS_HELPTEXTA","GCS_HELPTEXTW","GCS_VALIDATEA","GCS_VALIDATEW","GCS_VERBA","GCS_VERBW","GetCommandString","GetCommandString method [Windows Shell]","GetCommandString method [Windows Shell]","IContextMenu interface","IContextMenu interface [Windows Shell]","GetCommandString method","IContextMenu.GetCommandString","IContextMenu::GetCommandString","_win32_IContextMenu_GetCommandString","_win32_icontextmenu_win32_icontextmenu_getcommandstring_cpp","shell.IContextMenu_GetCommandString","shobjidl_core/IContextMenu::GetCommandString"]
old-location: shell\IContextMenu_GetCommandString.htm
tech.root: shell
ms.assetid: efa60153-7635-4aef-bd9e-f51fe4ecc234
ms.date: 12/05/2018
ms.keywords: GCS_HELPTEXTA, GCS_HELPTEXTW, GCS_VALIDATEA, GCS_VALIDATEW, GCS_VERBA, GCS_VERBW, GetCommandString, GetCommandString method [Windows Shell], GetCommandString method [Windows Shell],IContextMenu interface, IContextMenu interface [Windows Shell],GetCommandString method, IContextMenu.GetCommandString, IContextMenu::GetCommandString, _win32_IContextMenu_GetCommandString, _win32_icontextmenu_win32_icontextmenu_getcommandstring_cpp, shell.IContextMenu_GetCommandString, shobjidl_core/IContextMenu::GetCommandString
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextMenu::GetCommandString
 - shobjidl_core/IContextMenu::GetCommandString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IContextMenu.GetCommandString
---

# IContextMenu::GetCommandString


## -description

Gets information about a shortcut menu command, including the help string and the language-independent, or <i>canonical</i>, name for the command.

## -parameters

### -param idCmd

Type: <b>UINT_PTR</b>

Menu command identifier offset.

### -param uType

Type: <b>UINT</b>

Flags specifying the information to return. This parameter can have one of the following values.



#### GCS_HELPTEXTA

Sets <i>pszName</i> to an ANSI string containing the help text for the command.



#### GCS_HELPTEXTW

Sets <i>pszName</i> to a Unicode string containing the help text for the command.



#### GCS_VALIDATEA

Returns S_OK if the menu item exists, or S_FALSE otherwise.



#### GCS_VALIDATEW

Returns S_OK if the menu item exists, or S_FALSE otherwise.



#### GCS_VERBA

Sets <i>pszName</i> to an ANSI string containing the language-independent command name for the menu item.



#### GCS_VERBW

Sets <i>pszName</i> to a Unicode string containing the language-independent command name for the menu item.

### -param pReserved

Type: <b>UINT*</b>

Reserved. Applications must specify <b>NULL</b> when calling this method and handlers must ignore this parameter when called.

### -param pszName

Type: <b>LPSTR</b>

The address of the buffer to receive the null-terminated string being retrieved.

### -param cchMax

Type: <b>UINT</b>

Size of the buffer, in characters, to receive the null-terminated string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The language-independent command name, or <i>verb</i>, is a name that can be passed to the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a> method to activate a command by an application. The help text is a description of the command that Windows Explorer displays in its status bar. It should be reasonably short (under 40 characters).

Several common verbs can be identified by their canonical name, for instance, <i>open</i>, <i>print</i>, <i>delete</i>, and <i>rename</i>. Clients can compare the string pointed to by <i>pszName</i> against these canonical names to check for their presence on the shortcut menu.

Even though <i>pszName</i> is declared as an <b>LPSTR</b>, you must cast it to <b>UINT_PTR</b> and return a Unicode string if <i>uFlags</i> is set to either <b>GCS_HELPTEXTW</b> or <b>GCS_VERBW</b>. <b>GCS_UNICODE</b> can be used as a bitmask to test <i>uFlags</i> for 'W' and 'A' versions of the flag it contains.