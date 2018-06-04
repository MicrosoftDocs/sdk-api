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

# IParentAndItem::GetParentAndItem


## -description


Gets the parent of an item and the parent's child ID.


## -parameters




### -param ppidlParent [out, optional]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this method returns, contains the address of a PIDL that specifies the parent.


### -param ppsf [out, optional]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>**</b>

When this method returns, contains the address of a pointer to the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> that is the parent.


### -param ppidlChild [out, optional]

Type: <b>PITEMID_CHILD*</b>

When this method returns, contains the address of a child PIDL that identifies the <a href="https://msdn.microsoft.com/5cca426f-73fb-4b39-8eb0-16c01673c311">IParentAndItem</a> object relative to that specified by <i>ppsf</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 While <a href="https://msdn.microsoft.com/5cca426f-73fb-4b39-8eb0-16c01673c311">IParentAndItem</a> is typically implemented on IShellItems, it is not specific to <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.



