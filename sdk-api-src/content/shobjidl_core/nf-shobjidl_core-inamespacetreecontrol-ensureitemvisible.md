---
UID: NF:shobjidl_core.INameSpaceTreeControl.EnsureItemVisible
title: INameSpaceTreeControl::EnsureItemVisible
author: windows-sdk-content
description: Ensures that the given item is visible.
old-location: shell\INameSpaceTreeControl_EnsureItemVisible.htm
old-project: shell
ms.assetid: c0c40137-e19b-448c-a327-454b12a5604a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EnsureItemVisible, EnsureItemVisible method [Windows Shell], EnsureItemVisible method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],EnsureItemVisible method, INameSpaceTreeControl.EnsureItemVisible, INameSpaceTreeControl::EnsureItemVisible, _shell_INameSpaceTreeControl_EnsureItemVisible, shell.INameSpaceTreeControl_EnsureItemVisible, shobjidl_core/INameSpaceTreeControl::EnsureItemVisible
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControl.EnsureItemVisible
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# INameSpaceTreeControl::EnsureItemVisible


## -description


Ensures that the given item is visible.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the Shell item for which the visibility is being ensured.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



