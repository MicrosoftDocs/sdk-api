---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



