---
UID: NF:shobjidl_core.IPersistIDList.SetIDList
title: IPersistIDList::SetIDList (shobjidl_core.h)
author: windows-sdk-content
description: Sets a persisted item identifier list.
old-location: shell\IPersistIDList_SetIDList.htm
tech.root: shell
ms.assetid: 0f509a36-e9be-46ab-8c01-067e44379615
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPersistIDList interface [Windows Shell],SetIDList method, IPersistIDList.SetIDList, IPersistIDList::SetIDList, SetIDList, SetIDList method [Windows Shell], SetIDList method [Windows Shell],IPersistIDList interface, inet_IPersistIDList_SetIDList, shell.IPersistIDList_SetIDList, shobjidl_core/IPersistIDList::SetIDList
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IPersistIDList.SetIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



