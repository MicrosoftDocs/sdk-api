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

# ISyncMgrEnumItems::Next


## -description


Enumerates the next <i>celt</i> elements in the enumerator's list, returning them in <i>rgelt</i> along with the actual number of enumerated elements in <i>pceltFetched</i>.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of items in the array.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a>*</b>

The address of array containing items.


### -param pceltFetched [out]

Type: <b>ULONG*</b>

The address of variable containing actual number of items.


## -returns



Type: <b>HRESULT</b>

Return S_OK if the method succeeds.




## -remarks



E_NOTIMPL is not allowed as a return value. If an error value is returned, no entries in the <i>rgelt</i> array are valid on exit and require no release.



