---
UID: NF:shobjidl_core.INamespaceWalkCB.LeaveFolder
title: INamespaceWalkCB::LeaveFolder
author: windows-sdk-content
description: Called after a namespace walk through a folder. Use this method to perform any necessary cleanup following the actions performed by INamespaceWalkCB::EnterFolder or INamespaceWalkCB::FoundItem.
old-location: shell\INamespaceWalkCB_LeaveFolder.htm
tech.root: shell
ms.assetid: 307b0686-c4ec-40c6-8bd3-18a7aa790875
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INamespaceWalkCB interface [Windows Shell],LeaveFolder method, INamespaceWalkCB.LeaveFolder, INamespaceWalkCB::LeaveFolder, LeaveFolder, LeaveFolder method [Windows Shell], LeaveFolder method [Windows Shell],INamespaceWalkCB interface, _win32_INamespaceWalkCB_LeaveFolder, shell.INamespaceWalkCB_LeaveFolder, shobjidl_core/INamespaceWalkCB::LeaveFolder
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - INamespaceWalkCB.LeaveFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INamespaceWalkCB::LeaveFolder


## -description


Called after a namespace walk through a folder. Use this method to perform any necessary cleanup following the actions performed by <a href="https://msdn.microsoft.com/fd5c25f4-6e48-494b-9d5b-ba1d846ce4d2">INamespaceWalkCB::EnterFolder</a> or <a href="https://msdn.microsoft.com/d9f86764-6365-432e-9216-57fede3aec83">INamespaceWalkCB::FoundItem</a>.


## -parameters




### -param psf [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> object representing the parent of the folder designated by <i>pidl</i>.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A PIDL, relative to <i>psf</i>, of the folder being exited.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



