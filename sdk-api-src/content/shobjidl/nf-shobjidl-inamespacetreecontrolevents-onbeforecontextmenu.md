---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnBeforeContextMenu
title: INameSpaceTreeControlEvents::OnBeforeContextMenu (shobjidl.h)
author: windows-sdk-content
description: Called before a context menu is displayed; allows client to add additional menu entries.
old-location: shell\INameSpaceTreeControlEvents_OnBeforeContextMenu.htm
tech.root: shell
ms.assetid: aa243592-1cda-4844-8f3c-e9c62083fabb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnBeforeContextMenu method, INameSpaceTreeControlEvents.OnBeforeContextMenu, INameSpaceTreeControlEvents::OnBeforeContextMenu, OnBeforeContextMenu, OnBeforeContextMenu method [Windows Shell], OnBeforeContextMenu method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnBeforeContextMenu, shell.INameSpaceTreeControlEvents_OnBeforeContextMenu, shobjidl/INameSpaceTreeControlEvents::OnBeforeContextMenu
ms.topic: method
f1_keywords: 
 - "shobjidl/INameSpaceTreeControlEvents.OnBeforeContextMenu"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlEvents.OnBeforeContextMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INameSpaceTreeControlEvents::OnBeforeContextMenu


## -description


Called before a context menu is displayed; allows client to add additional menu entries.


## -parameters




### -param psi [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> from which the context menu is generated. This value can be <b>NULL</b>.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the IID of the context menu.


### -param ppv [out]

Type: <b>void**</b>

When this methods returns, contains the address of a pointer to the interface specified by <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>
 

 

