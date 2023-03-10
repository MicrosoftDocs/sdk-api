---
UID: NS:shlobj_core.DEFCONTEXTMENU
title: DEFCONTEXTMENU (shlobj_core.h)
description: Contains context menu information used by SHCreateDefaultContextMenu.
helpviewer_keywords: ["DEFCONTEXTMENU","DEFCONTEXTMENU structure [Windows Shell]","_shell_DEFCONTEXTMENU","shell.DEFCONTEXTMENU","shlobj_core/DEFCONTEXTMENU"]
old-location: shell\DEFCONTEXTMENU.htm
tech.root: shell
ms.assetid: 007861f6-1e66-4c5f-a459-3cfbe9f8cec2
ms.date: 12/05/2018
ms.keywords: DEFCONTEXTMENU, DEFCONTEXTMENU structure [Windows Shell], _shell_DEFCONTEXTMENU, shell.DEFCONTEXTMENU, shlobj_core/DEFCONTEXTMENU
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DEFCONTEXTMENU
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DEFCONTEXTMENU
 - shlobj_core/DEFCONTEXTMENU
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - DEFCONTEXTMENU
---

# DEFCONTEXTMENU structure


## -description

Contains context menu information used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu">SHCreateDefaultContextMenu</a>.

## -struct-fields

### -field hwnd

Type: <b>HWND</b>

A handle to the context menu. Set this member to the handle returned from <a href="/windows/desktop/api/winuser/nf-winuser-createmenu">CreateMenu</a>.

### -field pcmcb

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb">IContextMenuCB</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb">IContextMenuCB</a> interface supported by the callback object. This value is optional and can be <b>NULL</b>.

### -field pidlFolder

Type: <b>PCIDLIST_ABSOLUTE</b>

The PIDL of the folder that contains the selected file object(s) or the folder of the context menu if no file objects are selected. This value is optional and can be <b>NULL</b>, in which case the PIDL is computed from the <b>psf</b> member.

### -field psf

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface of the folder object that contains the selected file objects, or the folder that contains the context menu if no file objects are selected.

### -field cidl

Type: <b>UINT</b>

The count of items in member <b>apidl</b>.

### -field apidl

Type: <b>PCUITEMID_CHILD_ARRAY</b>

A pointer to a constant array of <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures. Each entry in the array describes a child item to which the context menu applies, for instance, a selected file the user wants to <b>Open</b>.

### -field punkAssociationInfo

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> interface on the object from which to load extensions. This parameter is optional and thus can be <b>NULL</b>. If this value is <b>NULL</b> and members <b>aKeys</b> and <b>cKeys</b> are also <b>NULL</b> (see Remarks),  <b>punkAssociationInfo</b> is computed from the <b>apidl</b> member and <b>cidl</b> via a request for <b>IQueryAssociations</b> through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a>.

If <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> returns <b>E_NOTIMPL</b>, a default implementation is provided based on the <i>SFGAO_FOLDER</i> and <i>SFGAO_FILESYSTEM</i> attributes returned from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>.

### -field cKeys

Type: <b>UINT</b>

The count of items in member <b>aKeys</b>. This value can be zero. If the value is zero, the extensions are loaded based on the object that supports interface <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> as specified by member <b>punkAssociationInfo</b>.  If the value is non-NULL, the extensions are loaded based only on member <b>aKeys</b> and not member <b>punkAssociationInfo</b>.

                    

<div class="alert"><b>Note</b>  The maximum number of keys is 16. Callers must enforce this limit as the API does not. Failing to do so can result in memory corruption.</div>
<div> </div>

### -field aKeys

Type: <b>const HKEY*</b>

A pointer to an HKEY that specifies the registry key from which to load extensions. This parameter is optional and can be <b>NULL</b>. If the value is <b>NULL</b>, the extensions are loaded based on the object that supports interface <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> as specified in <b>punkAssociationInfo</b>.

## -remarks

If the <b>aKeys</b> and <b>cKeys</b> members are valid and member <b>punkAssociationInfo</b> is also valid (not <b>NULL</b>), the system constructs the menu using the values of <b>aKeys</b> and <b>cKeys</b>, and ignores member <b>punkAssociationInfo</b> (<a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a>).

Members <b>apidl</b> and <b>cidl</b> can be used as parameters to method <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> to retrieve <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>.

