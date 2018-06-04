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

# SHCreateDefaultPropertiesOp function


## -description


Creates a file operation that sets the default properties on the Shell item that have not already been set.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the source shell item. See <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


### -param ppFileOp [out]

Type: <b><a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>**</b>

The address of the <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The list of properties to set a default value comes from the <b>SetDefaultsFor</b> registry entry under the ProgID for the file association of the item. The list is prefixed by <code>prop:</code> and contains the canonical names of the properties to set the default value, for example, <code>prop:System.Author;System.Document.DateCreated</code>. The possible properties for this list are <a href="https://msdn.microsoft.com/07a411c2-9e88-4d14-b9f7-e3a5d8d1630e">System.Author</a>, <a href="https://msdn.microsoft.com/00d8faa6-6b9c-4981-aeb1-17f8f14b1926">System.Document.DateCreated</a>, and <a href="https://msdn.microsoft.com/197fb739-7fe6-47e8-908f-54e75cb47ec4">System.Photo.DateTaken</a>. If the <b>SetDefaultsFor</b> entry does not exist on the ProgID, this function uses the default found on the <b>SetDefaultsFor</b> entry of <b>HKEY_CLASSES_ROOT</b>\<b>*</b>.



