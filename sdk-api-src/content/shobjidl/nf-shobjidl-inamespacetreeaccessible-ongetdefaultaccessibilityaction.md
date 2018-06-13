---
UID: NF:shobjidl.INameSpaceTreeAccessible.OnGetDefaultAccessibilityAction
title: INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction
author: windows-sdk-content
description: Gets the default accessibility action for a Shell item.
old-location: shell\INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction.htm
old-project: shell
ms.assetid: 96eaac9c-7fab-4326-a737-4819794a34c6
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: INameSpaceTreeAccessible interface [Windows Shell],OnGetDefaultAccessibilityAction method, INameSpaceTreeAccessible.OnGetDefaultAccessibilityAction, INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction, OnGetDefaultAccessibilityAction, OnGetDefaultAccessibilityAction method [Windows Shell], OnGetDefaultAccessibilityAction method [Windows Shell],INameSpaceTreeAccessible interface, _shell_INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction, shell.INameSpaceTreeAccessible_OnGetDefaultAccessibilityAction, shobjidl/INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction
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
 - INameSpaceTreeAccessible.OnGetDefaultAccessibilityAction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeAccessible::OnGetDefaultAccessibilityAction


## -description


Gets the default accessibility action for a Shell item.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


### -param pbstrDefaultAction [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>*</b>

When this method returns, contains a <a href="https://msdn.microsoft.com/library/windows/desktop/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> that specifies the default, accessibility action.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or E_OUTOFMEMORY otherwise.




## -remarks



This method is called when the default accessibililty action for a Shell item is retrieved.



