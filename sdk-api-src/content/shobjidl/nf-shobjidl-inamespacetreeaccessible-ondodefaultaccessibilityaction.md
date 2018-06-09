---
UID: NF:shobjidl.INameSpaceTreeAccessible.OnDoDefaultAccessibilityAction
title: INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction
author: windows-sdk-content
description: Invokes the default accessibility action on a Shell item.
old-location: shell\INameSpaceTreeAccessible_OnDoDefaultAccessibilityAction.htm
old-project: shell
ms.assetid: a6aa6588-6e3c-4229-8540-0aa5d85c0381
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: INameSpaceTreeAccessible interface [Windows Shell],OnDoDefaultAccessibilityAction method, INameSpaceTreeAccessible.OnDoDefaultAccessibilityAction, INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction, OnDoDefaultAccessibilityAction, OnDoDefaultAccessibilityAction method [Windows Shell], OnDoDefaultAccessibilityAction method [Windows Shell],INameSpaceTreeAccessible interface, _shell_INameSpaceTreeAccessible_OnDoDefaultAccessibilityAction, shell.INameSpaceTreeAccessible_OnDoDefaultAccessibilityAction, shobjidl/INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeAccessible.OnDoDefaultAccessibilityAction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeAccessible::OnDoDefaultAccessibilityAction


## -description


Invokes the default accessibility action on a Shell item.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



