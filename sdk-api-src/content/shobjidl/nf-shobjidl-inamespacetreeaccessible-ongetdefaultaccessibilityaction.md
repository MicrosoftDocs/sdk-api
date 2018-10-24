---
UID: NF:shobjidl.INameSpaceTreeAccessible.OnGetDefaultAccessibilityAction
title: INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction
author: windows-sdk-content
description: Gets the default accessibility action for a Shell item.
old-location: shell\INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction.htm
tech.root: shell
ms.assetid: 96eaac9c-7fab-4326-a737-4819794a34c6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: INameSpaceTreeAccessible interface [Windows Shell],OnGetDefaultAccessibilityAction method, INameSpaceTreeAccessible.OnGetDefaultAccessibilityAction, INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction, OnGetDefaultAccessibilityAction, OnGetDefaultAccessibilityAction method [Windows Shell], OnGetDefaultAccessibilityAction method [Windows Shell],INameSpaceTreeAccessible interface, _shell_INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction, shell.INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction, shobjidl/INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - INameSpaceTreeAccessible.OnGetDefaultAccessibilityAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction


## -description


Gets the default accessibility action for a Shell item.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


### -param pbstrDefaultAction [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a>*</b>

When this method returns, contains a <a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a> that specifies the default, accessibility action.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or E_OUTOFMEMORY otherwise.




## -remarks



This method is called when the default accessibililty action for a Shell item is retrieved.



