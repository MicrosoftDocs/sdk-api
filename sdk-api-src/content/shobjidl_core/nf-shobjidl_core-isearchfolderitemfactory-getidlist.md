---
UID: NF:shobjidl_core.ISearchFolderItemFactory.GetIDList
title: ISearchFolderItemFactory::GetIDList (shobjidl_core.h)
description: Gets the search folder as an ITEMIDLIST.
helpviewer_keywords: ["GetIDList","GetIDList method [Windows Shell]","GetIDList method [Windows Shell]","ISearchFolderItemFactory interface","ISearchFolderItemFactory interface [Windows Shell]","GetIDList method","ISearchFolderItemFactory.GetIDList","ISearchFolderItemFactory::GetIDList","_shell_ISearchFolderItemFactory_GetIDList","shell.ISearchFolderItemFactory_GetIDList","shobjidl_core/ISearchFolderItemFactory::GetIDList"]
old-location: shell\ISearchFolderItemFactory_GetIDList.htm
tech.root: shell
ms.assetid: 9547c429-9396-474e-b772-6e3aa28d1937
ms.date: 12/05/2018
ms.keywords: GetIDList, GetIDList method [Windows Shell], GetIDList method [Windows Shell],ISearchFolderItemFactory interface, ISearchFolderItemFactory interface [Windows Shell],GetIDList method, ISearchFolderItemFactory.GetIDList, ISearchFolderItemFactory::GetIDList, _shell_ISearchFolderItemFactory_GetIDList, shell.ISearchFolderItemFactory_GetIDList, shobjidl_core/ISearchFolderItemFactory::GetIDList
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
 - ISearchFolderItemFactory::GetIDList
 - shobjidl_core/ISearchFolderItemFactory::GetIDList
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
 - ISearchFolderItemFactory.GetIDList
---

# ISearchFolderItemFactory::GetIDList


## -description

Gets the search folder as an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

## -parameters

### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this method returns successfully, contains a PIDL.

## -returns

Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory">ISearchFolderItemFactory</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject">SHGetIDListFromObject</a>