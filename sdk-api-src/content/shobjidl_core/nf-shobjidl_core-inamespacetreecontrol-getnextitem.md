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

# INameSpaceTreeControl::GetNextItem


## -description


Retrieves the next item in the tree according to which method is requested.


## -parameters




### -param psi [in, optional]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

The Shell item for which the next item is being retrieved. This value can be <b>NULL</b>.


### -param nstcgi [in]

Type: <b>NSTCGNI</b>

The type of the next item. This value can be one of the following flags:



#### NSTCGNI_NEXT (0)

The next sibling of the given item.



#### NSTCGNI_NEXTVISIBLE (1)

The next visible item in the tree that has any relationship to the given item. This includes a child (if there is one), the next sibling, or even one of the ancestor's siblings.



#### NSTCGNI_PREV (2)

The previous sibling item of the given item.



#### NSTCGNI_PREVVISIBLE (3)

The previous visible item that is a sibling item, sibling descendent item or a parent item.



#### NSTCGNI_PARENT (4)

The parent item of the given item.



#### NSTCGNI_CHILD (5)

The first child item of the given item.



#### NSTCGNI_FIRSTVISIBLE (6)

The absolute first visible item in the tree (not relative to the given item).



#### NSTCGNI_LASTVISIBLE (7)

The absolute last visible item in the tree (not relative to the given item).


### -param ppsiNext [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

The address of a pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that fits the criteria for the next item that was requested.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If there is no next item for the type selected, this function returns E_FAIL with <b>NULL</b> for the returned item, <i>ppsiNext</i>.



