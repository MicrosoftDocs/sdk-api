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

# AssocCreateForClasses function


## -description


Retrieves an object that implements an <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface.


## -parameters




### -param rgClasses [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/dn934603">ASSOCIATIONELEMENT</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/dn934603">ASSOCIATIONELEMENT</a> structures.


### -param cClasses [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>rgClasses</i>.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID, normally IID_IQueryAssociations.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is normally <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For systems earlier than Windows Vista, use the <a href="https://msdn.microsoft.com/33099e0e-73e3-4047-804f-765a59e42e3f">AssocCreate</a> function.



