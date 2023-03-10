---
UID: NN:shobjidl_core.IKnownFolder
title: IKnownFolder (shobjidl_core.h)
description: Exposes methods that allow an application to retrieve information about a known folder's category, type, GUID, pointer to an item identifier list (PIDL) value, redirection capabilities, and definition.
helpviewer_keywords: ["IKnownFolder","IKnownFolder interface [Windows Shell]","IKnownFolder interface [Windows Shell]","described","_shell_IKnownFolder","shell.IKnownFolder","shobjidl_core/IKnownFolder"]
old-location: shell\IKnownFolder.htm
tech.root: shell
ms.assetid: dbade93d-73f6-401b-9986-4e6fd439c874
ms.date: 12/05/2018
ms.keywords: IKnownFolder, IKnownFolder interface [Windows Shell], IKnownFolder interface [Windows Shell],described, _shell_IKnownFolder, shell.IKnownFolder, shobjidl_core/IKnownFolder
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
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKnownFolder
 - shobjidl_core/IKnownFolder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolder
---

# IKnownFolder interface


## -description

Exposes methods that allow an application to retrieve information about a known folder's category, type, GUID, pointer to an item identifier list (PIDL) value, redirection capabilities, and definition. It provides a method for the retrieval of a known folder's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object. It also provides methods to get or set the path of the known folder.

## -inheritance

The <b>IKnownFolder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKnownFolder</b> also has these types of members:

## -remarks

<b>IKnownFolder</b> objects can be obtained through several methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a> interface, such as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolder">IKnownFolderManager::GetFolder</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-findfolderfromidlist">IKnownFolderManager::FindFolderFromIDList</a>.

Third parties do not implement <b>IKnownFolder</b>. Use the provided implementation.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>
