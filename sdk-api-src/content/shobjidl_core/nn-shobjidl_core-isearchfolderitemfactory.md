---
UID: NN:shobjidl_core.ISearchFolderItemFactory
title: ISearchFolderItemFactory (shobjidl_core.h)
description: Exposes methods that create and modify search folders.
helpviewer_keywords: ["ISearchFolderItemFactory","ISearchFolderItemFactory interface [Windows Shell]","ISearchFolderItemFactory interface [Windows Shell]","described","_shell_ISearchFolderItemFactory","shell.ISearchFolderItemFactory","shobjidl_core/ISearchFolderItemFactory"]
old-location: shell\ISearchFolderItemFactory.htm
tech.root: shell
ms.assetid: a684b373-6de4-4b4a-bbae-85e1c5a7e04a
ms.date: 12/05/2018
ms.keywords: ISearchFolderItemFactory, ISearchFolderItemFactory interface [Windows Shell], ISearchFolderItemFactory interface [Windows Shell],described, _shell_ISearchFolderItemFactory, shell.ISearchFolderItemFactory, shobjidl_core/ISearchFolderItemFactory
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
 - ISearchFolderItemFactory
 - shobjidl_core/ISearchFolderItemFactory
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
 - ISearchFolderItemFactory
---

# ISearchFolderItemFactory interface


## -description

Exposes methods that create and modify search folders. The Set methods are called first to set up the parameters of the search.  When not called, default values will be used instead.  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getidlist">ISearchFolderItemFactory::GetIDList</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getshellitem">ISearchFolderItemFactory::GetShellItem</a> return the two forms of the search specified by these parameters.

## -inheritance

The <b>ISearchFolderItemFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchFolderItemFactory</b> also has these types of members:

## -remarks

To implement this interface use class ID <b>CLSID_SearchFolderItemFactory</b>.
