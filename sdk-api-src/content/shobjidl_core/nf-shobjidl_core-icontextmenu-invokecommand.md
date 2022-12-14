---
UID: NF:shobjidl_core.IContextMenu.InvokeCommand
title: IContextMenu::InvokeCommand (shobjidl_core.h)
description: Carries out the command associated with a shortcut menu item.
helpviewer_keywords: ["IContextMenu interface [Windows Shell]","InvokeCommand method","IContextMenu.InvokeCommand","IContextMenu::InvokeCommand","InvokeCommand","InvokeCommand method [Windows Shell]","InvokeCommand method [Windows Shell]","IContextMenu interface","_win32_IContextMenu_InvokeCommand","_win32_icontextmenu_win32_icontextmenu_invokecommand_cpp","shell.IContextMenu_InvokeCommand","shobjidl_core/IContextMenu::InvokeCommand"]
old-location: shell\IContextMenu_InvokeCommand.htm
tech.root: shell
ms.assetid: f3aaa84c-3b33-4288-a46a-cd80d3fa89cf
ms.date: 12/05/2018
ms.keywords: IContextMenu interface [Windows Shell],InvokeCommand method, IContextMenu.InvokeCommand, IContextMenu::InvokeCommand, InvokeCommand, InvokeCommand method [Windows Shell], InvokeCommand method [Windows Shell],IContextMenu interface, _win32_IContextMenu_InvokeCommand, _win32_icontextmenu_win32_icontextmenu_invokecommand_cpp, shell.IContextMenu_InvokeCommand, shobjidl_core/IContextMenu::InvokeCommand
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
 - IContextMenu::InvokeCommand
 - shobjidl_core/IContextMenu::InvokeCommand
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
 - IContextMenu.InvokeCommand
---

# IContextMenu::InvokeCommand


## -description

Carries out the command associated with a shortcut menu item.

## -parameters

### -param pici

Type: <b>LPCMINVOKECOMMANDINFO</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo">CMINVOKECOMMANDINFO</a> or <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex">CMINVOKECOMMANDINFOEX</a> structure that contains specifics about the command.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> interface is exported by several Shell extension handlers and namespace extensions. It is used to add commands to shortcut menus. When the user selects one of the commands that the handler or namespace extension added to a shortcut menu, the Shell calls that command's <b>InvokeCommand</b> method. The command can be specified by its menu identifier offset, defined when <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu">IContextMenu::QueryContextMenu</a> was called, or by its associated verb. An application can invoke this method directly by obtaining a pointer to an object's <b>IContextMenu</b> interface. An application can also invoke this method indirectly by calling <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a> or <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> and specifying a verb that is supported by the namespace extension or handler.

<h3><a id="Note_to_Users"></a><a id="note_to_users"></a><a id="NOTE_TO_USERS"></a>Note to Users</h3>
Although the <i>pici</i> parameter is declared in Shlobj.h as a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo">CMINVOKECOMMANDINFO</a> structure, you can use either <b>CMINVOKECOMMANDINFO</b> or <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex">CMINVOKECOMMANDINFOEX</a>. Either will work for ANSI strings, but you must use a <b>CMINVOKECOMMANDINFOEX</b> structure for Unicode strings.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Check the <b>cbSize</b> member of <i>pici</i> to determine which structure (<a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo">CMINVOKECOMMANDINFO</a> or <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex">CMINVOKECOMMANDINFOEX</a>) was passed in. If it is a <b>CMINVOKECOMMANDINFOEX</b> structure and the <b>fMask</b> member has the <b>CMIC_MASK_UNICODE</b> flag set, you must cast <i>pici</i> to <b>CMINVOKECOMMANDINFOEX</b> to use the Unicode information contained in the last five members of the structure.

If the verb, specified either by a canonical verb name or the command ID is not recognized by the context menu handler, it must return a failure (E_FAIL) so that the verb can be passed on to other context menu handlers that might implement it.

As of Windows Vista, it is not sufficient invoke the command asynchronously simply by setting the CMIC_MASK_ASYNCOK flag in the <b>fMask</b> member of the <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo">CMINVOKECOMMANDINFO</a> or <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex">CMINVOKECOMMANDINFOEX</a> structure. You must also set a thread reference on the calling thread as explained in <a href="/windows/desktop/shell/managing-thread-references">Managing Thread References</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a>