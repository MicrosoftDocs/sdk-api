---
UID: NF:shobjidl_core.INameSpaceTreeControl.AppendRoot
title: INameSpaceTreeControl::AppendRoot
author: windows-sdk-content
description: Appends a Shell item to the list of roots in a tree.
old-location: shell\INameSpaceTreeControl_AppendRoot.htm
tech.root: shell
ms.assetid: a280d183-9215-43c2-bba3-63c34ba33285
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: AppendRoot, AppendRoot method [Windows Shell], AppendRoot method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],AppendRoot method, INameSpaceTreeControl.AppendRoot, INameSpaceTreeControl::AppendRoot, NSTCRS_EXPANDED, NSTCRS_HIDDEN, NSTCRS_VISIBLE, _shell_INameSpaceTreeControl_AppendRoot, shell.INameSpaceTreeControl_AppendRoot, shobjidl_core/INameSpaceTreeControl::AppendRoot
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControl.AppendRoot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControl::AppendRoot


## -description


Appends a Shell item to the list of roots in a tree.


## -parameters




### -param psiRoot [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to the Shell item that is being appended.


### -param grfEnumFlags [in]

Type: <b><a href="https://msdn.microsoft.com/a46845bf-ade6-4366-8a73-6dc960fd7722">SHCONTF</a></b>

Enumerates the qualities of the root and all of its children. One or more of the values of type <a href="https://msdn.microsoft.com/a46845bf-ade6-4366-8a73-6dc960fd7722">SHCONTF</a>. These flags can be combined using a bitwise OR.


### -param grfRootStyle [in]

Type: <b>NSTCROOTSTYLE</b>

Specifies the style of the root that is being appended. One or more of the following values:



#### NSTCRS_VISIBLE (0x0000)

The root is visible as well as the items.  Mutually exclusive with NSTCRS_HIDDEN.



#### NSTCRS_HIDDEN (0x0001)

The root is hidden so that the children only are visible. Mutually exclusive with NSTCRS_VISIBLE.



#### NSTCRS_EXPANDED (0x0002)

The root is expanded upon initialization.


### -param pif [in]

Type: <b><a href="https://msdn.microsoft.com/c2873385-a25d-4d9d-94ef-05dcdf284be1">IShellItemFilter</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/c2873385-a25d-4d9d-94ef-05dcdf284be1">IShellItemFilter</a> that enables you to filter which items in the tree are displayed. If supplied, every item is customizable with a <a href="https://msdn.microsoft.com/a46845bf-ade6-4366-8a73-6dc960fd7722">SHCONTF</a> flag. This value can be <b>NULL</b> if no filter is required.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



