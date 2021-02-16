---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetFolderLogicalViewMode
title: ISearchFolderItemFactory::SetFolderLogicalViewMode (shobjidl_core.h)
description: Sets folder logical view mode. The default settings are based on the FolderTypeID which is set by the ISearchFolderItemFactory::SetFolderTypeID method.
helpviewer_keywords: ["ISearchFolderItemFactory interface [Windows Shell]","SetFolderLogicalViewMode method","ISearchFolderItemFactory.SetFolderLogicalViewMode","ISearchFolderItemFactory::SetFolderLogicalViewMode","SetFolderLogicalViewMode","SetFolderLogicalViewMode method [Windows Shell]","SetFolderLogicalViewMode method [Windows Shell]","ISearchFolderItemFactory interface","_shell_ISearchFolderItemFactory_SetFolderLogicalViewMode","shell.ISearchFolderItemFactory_SetFolderLogicalViewMode","shobjidl_core/ISearchFolderItemFactory::SetFolderLogicalViewMode"]
old-location: shell\ISearchFolderItemFactory_SetFolderLogicalViewMode.htm
tech.root: shell
ms.assetid: ef72f196-cfd5-4547-85cb-0ccfdc496c46
ms.date: 12/05/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetFolderLogicalViewMode method, ISearchFolderItemFactory.SetFolderLogicalViewMode, ISearchFolderItemFactory::SetFolderLogicalViewMode, SetFolderLogicalViewMode, SetFolderLogicalViewMode method [Windows Shell], SetFolderLogicalViewMode method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetFolderLogicalViewMode, shell.ISearchFolderItemFactory_SetFolderLogicalViewMode, shobjidl_core/ISearchFolderItemFactory::SetFolderLogicalViewMode
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
 - ISearchFolderItemFactory::SetFolderLogicalViewMode
 - shobjidl_core/ISearchFolderItemFactory::SetFolderLogicalViewMode
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
 - ISearchFolderItemFactory.SetFolderLogicalViewMode
---

# ISearchFolderItemFactory::SetFolderLogicalViewMode


## -description

Sets folder logical view mode. The default settings are based on the <code>FolderTypeID</code> which is set by the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfoldertypeid">ISearchFolderItemFactory::SetFolderTypeID</a> method.

## -parameters

### -param flvm [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderlogicalviewmode">FOLDERLOGICALVIEWMODE</a></b>

The <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderlogicalviewmode">FOLDERLOGICALVIEWMODE</a> value.

## -returns

Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.