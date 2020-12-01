---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetStacks
title: ISearchFolderItemFactory::SetStacks (shobjidl_core.h)
description: Creates a list of stack keys, as specified. If this method is not called, by default the folder will not be stacked.
helpviewer_keywords: ["ISearchFolderItemFactory interface [Windows Shell]","SetStacks method","ISearchFolderItemFactory.SetStacks","ISearchFolderItemFactory::SetStacks","SetStacks","SetStacks method [Windows Shell]","SetStacks method [Windows Shell]","ISearchFolderItemFactory interface","_shell_ISearchFolderItemFactory_SetStacks","shell.ISearchFolderItemFactory_SetStacks","shobjidl_core/ISearchFolderItemFactory::SetStacks"]
old-location: shell\ISearchFolderItemFactory_SetStacks.htm
tech.root: shell
ms.assetid: d2f3d975-b968-4491-868f-90eccb40e8e4
ms.date: 12/05/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetStacks method, ISearchFolderItemFactory.SetStacks, ISearchFolderItemFactory::SetStacks, SetStacks, SetStacks method [Windows Shell], SetStacks method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetStacks, shell.ISearchFolderItemFactory_SetStacks, shobjidl_core/ISearchFolderItemFactory::SetStacks
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
 - ISearchFolderItemFactory::SetStacks
 - shobjidl_core/ISearchFolderItemFactory::SetStacks
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
 - ISearchFolderItemFactory.SetStacks
---

# ISearchFolderItemFactory::SetStacks


## -description

Creates a list of stack keys, as specified. If this method is not called, by default the folder will not be stacked.

## -parameters

### -param cStackKeys [in]

Type: <b>UINT</b>

The number of stacks keys.

### -param rgStackKeys [in]

Type: <b><a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures containing stack key information.

## -returns

Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.