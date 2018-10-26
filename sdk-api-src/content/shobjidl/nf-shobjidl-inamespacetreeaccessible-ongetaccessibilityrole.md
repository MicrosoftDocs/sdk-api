---
UID: NF:shobjidl.INameSpaceTreeAccessible.OnGetAccessibilityRole
title: INameSpaceTreeAccessible::OnGetAccessibilityRole
author: windows-sdk-content
description: Gets the accessibility role for a Shell item.
old-location: shell\INameSpaceTreeAccessible_OnGetAccessibilityRole.htm
tech.root: shell
ms.assetid: 9de27a09-dc11-46a6-a233-696ccf35aa87
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: INameSpaceTreeAccessible interface [Windows Shell],OnGetAccessibilityRole method, INameSpaceTreeAccessible.OnGetAccessibilityRole, INameSpaceTreeAccessible::OnGetAccessibilityRole, OnGetAccessibilityRole, OnGetAccessibilityRole method [Windows Shell], OnGetAccessibilityRole method [Windows Shell],INameSpaceTreeAccessible interface, _shell_INameSpaceTreeAccessible_OnGetAccessibilityRole, shell.INameSpaceTreeAccessible_OnGetAccessibilityRole, shobjidl/INameSpaceTreeAccessible::OnGetAccessibilityRole
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
 - INameSpaceTreeAccessible.OnGetAccessibilityRole
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeAccessible::OnGetAccessibilityRole


## -description


Gets the accessibility role for a Shell item.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


### -param pvarRole [out]

Type: <b>VARIANT*</b>

When this method returns, contains a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> that specifies the role.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called when the accessibility role for a Shell item is retrieved.



