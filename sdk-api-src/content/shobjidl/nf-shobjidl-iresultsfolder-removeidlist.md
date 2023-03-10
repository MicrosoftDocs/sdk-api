---
UID: NF:shobjidl.IResultsFolder.RemoveIDList
title: IResultsFolder::RemoveIDList (shobjidl.h)
description: Removes a pointer to an item identifier list (PIDL) from a results folder.
helpviewer_keywords: ["IResultsFolder interface [Windows Shell]","RemoveIDList method","IResultsFolder.RemoveIDList","IResultsFolder::RemoveIDList","RemoveIDList","RemoveIDList method [Windows Shell]","RemoveIDList method [Windows Shell]","IResultsFolder interface","_shell_IResultsFolder_RemoveIDList","shell.IResultsFolder_RemoveIDList","shobjidl/IResultsFolder::RemoveIDList"]
old-location: shell\IResultsFolder_RemoveIDList.htm
tech.root: shell
ms.assetid: 188d4f7f-954c-4bba-ad4e-164085e0cc5a
ms.date: 12/05/2018
ms.keywords: IResultsFolder interface [Windows Shell],RemoveIDList method, IResultsFolder.RemoveIDList, IResultsFolder::RemoveIDList, RemoveIDList, RemoveIDList method [Windows Shell], RemoveIDList method [Windows Shell],IResultsFolder interface, _shell_IResultsFolder_RemoveIDList, shell.IResultsFolder_RemoveIDList, shobjidl/IResultsFolder::RemoveIDList
req.header: shobjidl.h
req.include-header: 
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
 - IResultsFolder::RemoveIDList
 - shobjidl/IResultsFolder::RemoveIDList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IResultsFolder.RemoveIDList
---

# IResultsFolder::RemoveIDList


## -description

Removes a pointer to an item identifier list (PIDL) from a results folder.

## -parameters

### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL relative to the Desktop.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

