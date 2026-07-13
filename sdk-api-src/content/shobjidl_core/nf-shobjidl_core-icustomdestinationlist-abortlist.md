---
UID: NF:shobjidl_core.ICustomDestinationList.AbortList
title: ICustomDestinationList::AbortList (shobjidl_core.h)
description: Discontinues a Jump List building session initiated by ICustomDestinationList::BeginList without committing any changes.
helpviewer_keywords: ["AbortList","AbortList method [Windows Shell]","AbortList method [Windows Shell]","ICustomDestinationList interface","ICustomDestinationList interface [Windows Shell]","AbortList method","ICustomDestinationList.AbortList","ICustomDestinationList::AbortList","_shell_ICustomDestinationList_AbortList","shell.ICustomDestinationList_AbortList","shobjidl_core/ICustomDestinationList::AbortList"]
old-location: shell\ICustomDestinationList_AbortList.htm
tech.root: shell
ms.assetid: 922eb957-8031-4b4c-9b13-78a86f199bfa
ms.date: 12/05/2018
ms.keywords: AbortList, AbortList method [Windows Shell], AbortList method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],AbortList method, ICustomDestinationList.AbortList, ICustomDestinationList::AbortList, _shell_ICustomDestinationList_AbortList, shell.ICustomDestinationList_AbortList, shobjidl_core/ICustomDestinationList::AbortList
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICustomDestinationList::AbortList
 - shobjidl_core/ICustomDestinationList::AbortList
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
 - ICustomDestinationList.AbortList
---

# ICustomDestinationList::AbortList


## -description

Discontinues a Jump List building session initiated by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a> without committing any changes.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method allows an application to use a single <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist">ICustomDestinationList</a> object for many transactions, because a session can be terminated without committing any new data or destroying the previously stored list.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist">ICustomDestinationList</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
