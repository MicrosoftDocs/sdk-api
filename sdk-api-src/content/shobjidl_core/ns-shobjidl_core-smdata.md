---
UID: NS:shobjidl_core.tagSMDATA
title: SMDATA (shobjidl_core.h)
description: Contains information from a menu band.
helpviewer_keywords: ["*LPSMDATA","SMDATA","SMDATA structure [Windows Shell]","_win32_SMDATA","lPSMDATA","lPSMDATA structure pointer [Windows Shell]","shell.SMDATA","shobjidl_core/SMDATA","shobjidl_core/lPSMDATA","tagSMDATA"]
old-location: shell\SMDATA.htm
tech.root: shell
ms.assetid: 4690daa1-f935-4d0c-8b1f-0b9442fc78dc
ms.date: 12/05/2018
ms.keywords: '*LPSMDATA, SMDATA, SMDATA structure [Windows Shell], _win32_SMDATA, lPSMDATA, lPSMDATA structure pointer [Windows Shell], shell.SMDATA, shobjidl_core/SMDATA, shobjidl_core/lPSMDATA, tagSMDATA'
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SMDATA, *LPSMDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSMDATA
 - shobjidl_core/tagSMDATA
 - LPSMDATA
 - shobjidl_core/LPSMDATA
 - SMDATA
 - shobjidl_core/SMDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - SMDATA
---

# SMDATA structure


## -description

Contains information from a menu band.

## -struct-fields

### -field dwMask

Type: <b>DWORD</b>

A mask that is always set to SMDM_HMENU.

### -field dwFlags

Type: <b>DWORD</b>

### -field hmenu

Type: <b>HMENU</b>

The static menu portion of the menu band.

### -field hwnd

Type: <b>HWND</b>

The HWND value of the owner window.

### -field uId

Type: <b>UINT</b>

The identifier of the menu item. This value is -1 for the menu itself.

### -field uIdParent

Type: <b>UINT</b>

The identifier of the parent menu.

### -field uIdAncestor

Type: <b>UINT</b>

### -field punk

Type: <b>IUnknown*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the <a href="/windows/desktop/shell/profiles-directory">MenuBand</a> object.

### -field pidlFolder

Type: <b>PIDLIST_ABSOLUTE</b>

The <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> of the shell folder portion of the menu.

### -field pidlItem

Type: <b>PUITEMID_CHILD</b>

The <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> of the selected item in the shell folder portion of the menu.

### -field psf

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface for the folder associated with the shell folder portion of the menu.

### -field pvUserData

Type: <b>void*</b>

A pointer to a user-defined data structure.