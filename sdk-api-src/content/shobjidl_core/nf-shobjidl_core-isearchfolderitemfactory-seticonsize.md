---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetIconSize
title: ISearchFolderItemFactory::SetIconSize (shobjidl_core.h)
description: Sets the search folder icon size, as specified. The default settings are based on the FolderTypeID which is set by the ISearchFolderItemFactory::SetFolderTypeID method.
helpviewer_keywords: ["ISearchFolderItemFactory interface [Windows Shell]","SetIconSize method","ISearchFolderItemFactory.SetIconSize","ISearchFolderItemFactory::SetIconSize","SetIconSize","SetIconSize method [Windows Shell]","SetIconSize method [Windows Shell]","ISearchFolderItemFactory interface","_shell_ISearchFolderItemFactory_SetIconSize","shell.ISearchFolderItemFactory_SetIconSize","shobjidl_core/ISearchFolderItemFactory::SetIconSize"]
old-location: shell\ISearchFolderItemFactory_SetIconSize.htm
tech.root: shell
ms.assetid: a9a6650f-d9fe-43e8-aed5-9a7006883148
ms.date: 12/05/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetIconSize method, ISearchFolderItemFactory.SetIconSize, ISearchFolderItemFactory::SetIconSize, SetIconSize, SetIconSize method [Windows Shell], SetIconSize method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetIconSize, shell.ISearchFolderItemFactory_SetIconSize, shobjidl_core/ISearchFolderItemFactory::SetIconSize
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchFolderItemFactory::SetIconSize
 - shobjidl_core/ISearchFolderItemFactory::SetIconSize
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
 - ISearchFolderItemFactory.SetIconSize
---

# ISearchFolderItemFactory::SetIconSize


## -description

Sets the search folder icon size, as specified. The default settings are based on the <code>FolderTypeID</code> which is set by the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfoldertypeid">ISearchFolderItemFactory::SetFolderTypeID</a> method.

## -parameters

### -param iIconSize [in]

Type: <b>int</b>

The icon size.

## -returns

Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.