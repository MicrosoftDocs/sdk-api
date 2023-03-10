---
UID: NF:shobjidl_core.IDefaultFolderMenuInitialize.GetMenuRestrictions
title: IDefaultFolderMenuInitialize::GetMenuRestrictions (shobjidl_core.h)
description: . (IDefaultFolderMenuInitialize.GetMenuRestrictions)
helpviewer_keywords: ["GetMenuRestrictions","GetMenuRestrictions method [Windows Shell]","GetMenuRestrictions method [Windows Shell]","IDefaultFolderMenuInitialize interface","IDefaultFolderMenuInitialize interface [Windows Shell]","GetMenuRestrictions method","IDefaultFolderMenuInitialize.GetMenuRestrictions","IDefaultFolderMenuInitialize::GetMenuRestrictions","shell.IDefaultFolderMenuInitialize_GetMenuRestrictions","shobjidl_core/IDefaultFolderMenuInitialize::GetMenuRestrictions"]
old-location: shell\IDefaultFolderMenuInitialize_GetMenuRestrictions.htm
tech.root: shell
ms.assetid: 373240B8-E99E-4ff9-B47A-3B31B4F0B81E
ms.date: 12/05/2018
ms.keywords: GetMenuRestrictions, GetMenuRestrictions method [Windows Shell], GetMenuRestrictions method [Windows Shell],IDefaultFolderMenuInitialize interface, IDefaultFolderMenuInitialize interface [Windows Shell],GetMenuRestrictions method, IDefaultFolderMenuInitialize.GetMenuRestrictions, IDefaultFolderMenuInitialize::GetMenuRestrictions, shell.IDefaultFolderMenuInitialize_GetMenuRestrictions, shobjidl_core/IDefaultFolderMenuInitialize::GetMenuRestrictions
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDefaultFolderMenuInitialize::GetMenuRestrictions
 - shobjidl_core/IDefaultFolderMenuInitialize::GetMenuRestrictions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDefaultFolderMenuInitialize.GetMenuRestrictions
---

# IDefaultFolderMenuInitialize::GetMenuRestrictions


## -description

Gets shortcut menu restrictions that are currently set for the [IDefaultFolderMenuInitialize](nn-shobjidl_core-idefaultfoldermenuinitialize.md) object.

## -parameters

### -param dfmrMask [in]

A bitwise combination of the [DEFAULT_FOLDER_MENU_RESTRICTIONS](ne-shobjidl_core-default_folder_menu_restrictions.md) values that specify the mask of the restrictions to get.

### -param pdfmrValues [out]

A bitwise combination of the [DEFAULT_FOLDER_MENU_RESTRICTIONS](ne-shobjidl_core-default_folder_menu_restrictions.md) values that specify the restrictions.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize">IDefaultFolderMenuInitialize</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultfoldermenuinitialize-setmenurestrictions">IDefaultFolderMenuInitialize::SetMenuRestrictions</a>
