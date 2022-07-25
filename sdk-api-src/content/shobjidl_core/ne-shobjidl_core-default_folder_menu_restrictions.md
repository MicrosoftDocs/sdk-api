---
UID: NE:shobjidl_core.DEFAULT_FOLDER_MENU_RESTRICTIONS
title: DEFAULT_FOLDER_MENU_RESTRICTIONS (shobjidl_core.h)
description: .
helpviewer_keywords: ["DEFAULT_FOLDER_MENU_RESTRICTIONS","DEFAULT_FOLDER_MENU_RESTRICTIONS enumeration [Windows Shell]","DFMR_DEFAULT","DFMR_NO_ASYNC_VERBS","DFMR_NO_RESOURCE_VERBS","DFMR_NO_STATIC_VERBS","DFMR_OPTIN_HANDLERS_ONLY","DFMR_RESOURCE_AND_FOLDER_VERBS_ONLY","DFMR_STATIC_VERBS_ONLY","DFMR_USE_SPECIFIED_HANDLERS","DFMR_USE_SPECIFIED_VERBS","shell.DEFAULT_FOLDER_MENU_RESTRICTIONS","shobjidl_core/DEFAULT_FOLDER_MENU_RESTRICTIONS","shobjidl_core/DFMR_DEFAULT","shobjidl_core/DFMR_NO_ASYNC_VERBS","shobjidl_core/DFMR_NO_RESOURCE_VERBS","shobjidl_core/DFMR_NO_STATIC_VERBS","shobjidl_core/DFMR_OPTIN_HANDLERS_ONLY","shobjidl_core/DFMR_RESOURCE_AND_FOLDER_VERBS_ONLY","shobjidl_core/DFMR_STATIC_VERBS_ONLY","shobjidl_core/DFMR_USE_SPECIFIED_HANDLERS","shobjidl_core/DFMR_USE_SPECIFIED_VERBS"]
old-location: shell\DEFAULT_FOLDER_MENU_RESTRICTIONS.htm
tech.root: shell
ms.assetid: E33EB02B-11FC-4c1f-AF38-0E5382CC8B5F
ms.date: 12/05/2018
ms.keywords: DEFAULT_FOLDER_MENU_RESTRICTIONS, DEFAULT_FOLDER_MENU_RESTRICTIONS enumeration [Windows Shell], DFMR_DEFAULT, DFMR_NO_ASYNC_VERBS, DFMR_NO_RESOURCE_VERBS, DFMR_NO_STATIC_VERBS, DFMR_OPTIN_HANDLERS_ONLY, DFMR_RESOURCE_AND_FOLDER_VERBS_ONLY, DFMR_STATIC_VERBS_ONLY, DFMR_USE_SPECIFIED_HANDLERS, DFMR_USE_SPECIFIED_VERBS, shell.DEFAULT_FOLDER_MENU_RESTRICTIONS, shobjidl_core/DEFAULT_FOLDER_MENU_RESTRICTIONS, shobjidl_core/DFMR_DEFAULT, shobjidl_core/DFMR_NO_ASYNC_VERBS, shobjidl_core/DFMR_NO_RESOURCE_VERBS, shobjidl_core/DFMR_NO_STATIC_VERBS, shobjidl_core/DFMR_OPTIN_HANDLERS_ONLY, shobjidl_core/DFMR_RESOURCE_AND_FOLDER_VERBS_ONLY, shobjidl_core/DFMR_STATIC_VERBS_ONLY, shobjidl_core/DFMR_USE_SPECIFIED_HANDLERS, shobjidl_core/DFMR_USE_SPECIFIED_VERBS
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DEFAULT_FOLDER_MENU_RESTRICTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DEFAULT_FOLDER_MENU_RESTRICTIONS
 - shobjidl_core/DEFAULT_FOLDER_MENU_RESTRICTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - DEFAULT_FOLDER_MENU_RESTRICTIONS
---

# DEFAULT_FOLDER_MENU_RESTRICTIONS enumeration


## -description

Defines shortcut menu restrictions used by [IDefaultFolderMenuInitialize::GetMenuRestrictions](nf-shobjidl_core-idefaultfoldermenuinitialize-getmenurestrictions.md) and [IDefaultFolderMenuInitialize::SetMenuRestrictions](nf-shobjidl_core-idefaultfoldermenuinitialize-setmenurestrictions.md).

## -enum-fields

### -field DFMR_DEFAULT:0

0x0000. No restrictions.

### -field DFMR_NO_STATIC_VERBS:0x8

0x0008. Don't use the handler for static verbs.

### -field DFMR_STATIC_VERBS_ONLY:0x10

0x0010. Static verbs only. No dynamic **IContextMenu** verbs allowed.

### -field DFMR_NO_RESOURCE_VERBS:0x20

0x0020. Don't add verbs for cut, copy, paste, link, delete, rename, or properties.

### -field DFMR_OPTIN_HANDLERS_ONLY:0x40

0x0040. Opt-in to load handler for partial cloud files. Only used for handlers that will not cause implicit hydration. Opt-in handlers must have the registry value "ContextMenuOptIn" under HKCR\CLSID\<handler clsid>

### -field DFMR_RESOURCE_AND_FOLDER_VERBS_ONLY:0x80

0x0080. Only load resource verbs (cut, copy, paste, link, delete, rename, and properties) and folder verbs added by [IContextMenuCB](nn-shobjidl_core-icontextmenucb.md).

### -field DFMR_USE_SPECIFIED_HANDLERS:0x100

0x0100. Use handlers with CLSID values that were added through [IDefaultFolderMenuInitialize::SetHandlerClsid](nf-shobjidl_core-idefaultfoldermenuinitialize-sethandlerclsid.md)

### -field DFMR_USE_SPECIFIED_VERBS:0x200

0x0200. Only load handlers that support the specified verbs.

### -field DFMR_NO_ASYNC_VERBS:0x400

0x0400. Ignore async verbs.

### -field DFMR_NO_NATIVECPU_VERBS:0x800

0x0800. Ignore verbs that are registered for the native CPU architecture.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultfoldermenuinitialize-getmenurestrictions">IDefaultFolderMenuInitialize::GetMenuRestrictions</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultfoldermenuinitialize-setmenurestrictions">IDefaultFolderMenuInitialize::SetMenuRestrictions</a>
