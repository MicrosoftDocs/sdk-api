---
UID: NF:shobjidl_core.ICustomDestinationList.CommitList
title: ICustomDestinationList::CommitList (shobjidl_core.h)
description: Declares that the Jump List initiated by a call to ICustomDestinationList::BeginList is complete and ready for display.
helpviewer_keywords: ["CommitList","CommitList method [Windows Shell]","CommitList method [Windows Shell]","ICustomDestinationList interface","ICustomDestinationList interface [Windows Shell]","CommitList method","ICustomDestinationList.CommitList","ICustomDestinationList::CommitList","_shell_ICustomDestinationList_CommitList","shell.ICustomDestinationList_CommitList","shobjidl_core/ICustomDestinationList::CommitList"]
old-location: shell\ICustomDestinationList_CommitList.htm
tech.root: shell
ms.assetid: 5f9aa598-9a94-4210-84cd-f4b39e47b260
ms.date: 12/05/2018
ms.keywords: CommitList, CommitList method [Windows Shell], CommitList method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],CommitList method, ICustomDestinationList.CommitList, ICustomDestinationList::CommitList, _shell_ICustomDestinationList_CommitList, shell.ICustomDestinationList_CommitList, shobjidl_core/ICustomDestinationList::CommitList
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
 - ICustomDestinationList::CommitList
 - shobjidl_core/ICustomDestinationList::CommitList
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
 - ICustomDestinationList.CommitList
---

# ICustomDestinationList::CommitList


## -description

Declares that the Jump List initiated by a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a> is complete and ready for display.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

As long as no call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory">AppendCategory</a> in this session failed for attempting to include a removed item, calling <b>CommitList</b> causes the stored list of removed items to be cleared and a new list of removed items to begin.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist">ICustomDestinationList</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
