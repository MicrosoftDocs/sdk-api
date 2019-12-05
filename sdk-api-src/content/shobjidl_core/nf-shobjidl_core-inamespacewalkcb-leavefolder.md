---
UID: NF:shobjidl_core.INamespaceWalkCB.LeaveFolder
title: INamespaceWalkCB::LeaveFolder (shobjidl_core.h)
description: Called after a namespace walk through a folder. Use this method to perform any necessary cleanup following the actions performed by INamespaceWalkCB::EnterFolder or INamespaceWalkCB::FoundItem.
old-location: shell\INamespaceWalkCB_LeaveFolder.htm
tech.root: shell
ms.assetid: 307b0686-c4ec-40c6-8bd3-18a7aa790875
ms.date: 12/05/2018
ms.keywords: INamespaceWalkCB interface [Windows Shell],LeaveFolder method, INamespaceWalkCB.LeaveFolder, INamespaceWalkCB::LeaveFolder, LeaveFolder, LeaveFolder method [Windows Shell], LeaveFolder method [Windows Shell],INamespaceWalkCB interface, _win32_INamespaceWalkCB_LeaveFolder, shell.INamespaceWalkCB_LeaveFolder, shobjidl_core/INamespaceWalkCB::LeaveFolder
ms.topic: method
f1_keywords:
- shobjidl_core/INamespaceWalkCB.LeaveFolder
dev_langs:
- c++
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
- INamespaceWalkCB.LeaveFolder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INamespaceWalkCB::LeaveFolder


## -description


Called after a namespace walk through a folder. Use this method to perform any necessary cleanup following the actions performed by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalkcb-enterfolder">INamespaceWalkCB::EnterFolder</a> or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalkcb-founditem">INamespaceWalkCB::FoundItem</a>.


## -parameters




### -param psf [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object representing the parent of the folder designated by <i>pidl</i>.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A PIDL, relative to <i>psf</i>, of the folder being exited.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



