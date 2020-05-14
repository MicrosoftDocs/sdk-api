---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetFolderTypeID
title: ISearchFolderItemFactory::SetFolderTypeID (shobjidl_core.h)
description: Sets a search folder type ID, as specified.helpviewer_keywords: ["ISearchFolderItemFactory interface [Windows Shell]","SetFolderTypeID method","ISearchFolderItemFactory.SetFolderTypeID","ISearchFolderItemFactory::SetFolderTypeID","SetFolderTypeID","SetFolderTypeID method [Windows Shell]","SetFolderTypeID method [Windows Shell]","ISearchFolderItemFactory interface","_shell_ISearchFolderItemFactory_SetFolderTypeID","shell.ISearchFolderItemFactory_SetFolderTypeID","shobjidl_core/ISearchFolderItemFactory::SetFolderTypeID"]
old-location: shell\ISearchFolderItemFactory_SetFolderTypeID.htm
tech.root: shell
ms.assetid: a9b09dc6-751e-4d5f-b016-0b26c15c68f6
ms.date: 12/05/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetFolderTypeID method, ISearchFolderItemFactory.SetFolderTypeID, ISearchFolderItemFactory::SetFolderTypeID, SetFolderTypeID, SetFolderTypeID method [Windows Shell], SetFolderTypeID method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetFolderTypeID, shell.ISearchFolderItemFactory_SetFolderTypeID, shobjidl_core/ISearchFolderItemFactory::SetFolderTypeID
f1_keywords:
- shobjidl_core/ISearchFolderItemFactory.SetFolderTypeID
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- ISearchFolderItemFactory.SetFolderTypeID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISearchFolderItemFactory::SetFolderTypeID


## -description


Sets a search folder type ID, as specified.


## -parameters




### -param ftid [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/shell/foldertypeid">FOLDERTYPEID</a></b>

The FOLDERTYPEID, which is a <b>GUID</b> used to identify folder types within the system. The default is <b>FOLDERTYPID_Library</b>


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.



