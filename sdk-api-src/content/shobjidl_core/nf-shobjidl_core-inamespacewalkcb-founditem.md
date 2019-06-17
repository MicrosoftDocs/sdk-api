---
UID: NF:shobjidl_core.INamespaceWalkCB.FoundItem
title: INamespaceWalkCB::FoundItem (shobjidl_core.h)
author: windows-sdk-content
description: Called when an object is found in the namespace during a namespace walk. Use this method as the main action function for the class implementing it. Perform your actions as needed inside this method.
old-location: shell\INamespaceWalkCB_FoundItem.htm
tech.root: shell
ms.assetid: d9f86764-6365-432e-9216-57fede3aec83
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FoundItem, FoundItem method [Windows Shell], FoundItem method [Windows Shell],INamespaceWalkCB interface, INamespaceWalkCB interface [Windows Shell],FoundItem method, INamespaceWalkCB.FoundItem, INamespaceWalkCB::FoundItem, _win32_INamespaceWalkCB_FoundItem, shell.INamespaceWalkCB_FoundItem, shobjidl_core/INamespaceWalkCB::FoundItem
ms.topic: method
f1_keywords: ["shobjidl_core/INamespaceWalkCB.FoundItem"]
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
 - INamespaceWalkCB.FoundItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INamespaceWalkCB::FoundItem


## -description


Called when an object is found in the namespace during a namespace walk. Use this method as the main action function for the class implementing it. Perform your actions as needed inside this method.


## -parameters




### -param psf [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object representing the folder containing the item.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

The item's PIDL, relative to <i>psf</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



