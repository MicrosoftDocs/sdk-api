---
UID: NF:shobjidl_core.IPersistIDList.SetIDList
title: IPersistIDList::SetIDList (shobjidl_core.h)
description: Sets a persisted item identifier list.
helpviewer_keywords: ["IPersistIDList interface [Windows Shell]","SetIDList method","IPersistIDList.SetIDList","IPersistIDList::SetIDList","SetIDList","SetIDList method [Windows Shell]","SetIDList method [Windows Shell]","IPersistIDList interface","inet_IPersistIDList_SetIDList","shell.IPersistIDList_SetIDList","shobjidl_core/IPersistIDList::SetIDList"]
old-location: shell\IPersistIDList_SetIDList.htm
tech.root: shell
ms.assetid: 0f509a36-e9be-46ab-8c01-067e44379615
ms.date: 12/05/2018
ms.keywords: IPersistIDList interface [Windows Shell],SetIDList method, IPersistIDList.SetIDList, IPersistIDList::SetIDList, SetIDList, SetIDList method [Windows Shell], SetIDList method [Windows Shell],IPersistIDList interface, inet_IPersistIDList_SetIDList, shell.IPersistIDList_SetIDList, shobjidl_core/IPersistIDList::SetIDList
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistIDList::SetIDList
 - shobjidl_core/IPersistIDList::SetIDList
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
 - IPersistIDList.SetIDList
---

# IPersistIDList::SetIDList


## -description

Sets a persisted item identifier list.

## -parameters

### -param pidl [in]

Type: <b>LPCITEMIDLIST</b>

A pointer to the item identifier list to set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

