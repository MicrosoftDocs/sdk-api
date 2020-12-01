---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetCondition
title: ISearchFolderItemFactory::SetCondition (shobjidl_core.h)
description: Sets the ICondition of the search. When this method is not called, the resulting search will have no filters applied.
helpviewer_keywords: ["ISearchFolderItemFactory interface [Windows Shell]","SetCondition method","ISearchFolderItemFactory.SetCondition","ISearchFolderItemFactory::SetCondition","SetCondition","SetCondition method [Windows Shell]","SetCondition method [Windows Shell]","ISearchFolderItemFactory interface","_shell_ISearchFolderItemFactory_SetCondition","shell.ISearchFolderItemFactory_SetCondition","shobjidl_core/ISearchFolderItemFactory::SetCondition"]
old-location: shell\ISearchFolderItemFactory_SetCondition.htm
tech.root: shell
ms.assetid: 6ac5acc3-e522-4b6f-a31c-c0850445e00c
ms.date: 12/05/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetCondition method, ISearchFolderItemFactory.SetCondition, ISearchFolderItemFactory::SetCondition, SetCondition, SetCondition method [Windows Shell], SetCondition method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetCondition, shell.ISearchFolderItemFactory_SetCondition, shobjidl_core/ISearchFolderItemFactory::SetCondition
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
 - ISearchFolderItemFactory::SetCondition
 - shobjidl_core/ISearchFolderItemFactory::SetCondition
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
 - ISearchFolderItemFactory.SetCondition
---

# ISearchFolderItemFactory::SetCondition


## -description

Sets the  <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> of the search.  When this method is not called, the resulting search will have no filters applied.

## -parameters

### -param pCondition [in]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>*</b>

A pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> interface.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone">ICondition::Clone</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory">ISearchFolderItemFactory</a>