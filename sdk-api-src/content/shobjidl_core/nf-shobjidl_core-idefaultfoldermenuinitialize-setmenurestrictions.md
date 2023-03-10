---
UID: NF:shobjidl_core.IDefaultFolderMenuInitialize.SetMenuRestrictions
title: IDefaultFolderMenuInitialize::SetMenuRestrictions (shobjidl_core.h)
description: . (IDefaultFolderMenuInitialize.SetMenuRestrictions)
helpviewer_keywords: ["IDefaultFolderMenuInitialize interface [Windows Shell]","SetMenuRestrictions method","IDefaultFolderMenuInitialize.SetMenuRestrictions","IDefaultFolderMenuInitialize::SetMenuRestrictions","SetMenuRestrictions","SetMenuRestrictions method [Windows Shell]","SetMenuRestrictions method [Windows Shell]","IDefaultFolderMenuInitialize interface","shell.IDefaultFolderMenuInitialize_SetMenuRestrictions","shobjidl_core/IDefaultFolderMenuInitialize::SetMenuRestrictions"]
old-location: shell\IDefaultFolderMenuInitialize_SetMenuRestrictions.htm
tech.root: shell
ms.assetid: 7D907B01-E0C4-428b-A8A4-FA383B0970BF
ms.date: 12/05/2018
ms.keywords: IDefaultFolderMenuInitialize interface [Windows Shell],SetMenuRestrictions method, IDefaultFolderMenuInitialize.SetMenuRestrictions, IDefaultFolderMenuInitialize::SetMenuRestrictions, SetMenuRestrictions, SetMenuRestrictions method [Windows Shell], SetMenuRestrictions method [Windows Shell],IDefaultFolderMenuInitialize interface, shell.IDefaultFolderMenuInitialize_SetMenuRestrictions, shobjidl_core/IDefaultFolderMenuInitialize::SetMenuRestrictions
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
 - IDefaultFolderMenuInitialize::SetMenuRestrictions
 - shobjidl_core/IDefaultFolderMenuInitialize::SetMenuRestrictions
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
 - IDefaultFolderMenuInitialize.SetMenuRestrictions
---

# IDefaultFolderMenuInitialize::SetMenuRestrictions


## -description

Sets shortcut menu restrictions for the [IDefaultFolderMenuInitialize](nn-shobjidl_core-idefaultfoldermenuinitialize.md) object.

## -parameters

### -param dfmrValues [in]

A bitwise combination of the [DEFAULT_FOLDER_MENU_RESTRICTIONS](ne-shobjidl_core-default_folder_menu_restrictions.md) values that specify the restrictions to set.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize">IDefaultFolderMenuInitialize</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultfoldermenuinitialize-getmenurestrictions">IDefaultFolderMenuInitialize::GetMenuRestrictions</a>
