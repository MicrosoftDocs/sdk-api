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

# ISyncMgrEnumItems::Skip


## -description


Instructs the enumerator to skip the next <i>celt</i> elements in the enumeration so that the next call to <a href="https://msdn.microsoft.com/bb4ab08a-aa12-46f0-8c7d-82742b0b1538">ISyncMgrEnumItems::Next</a> does not return those elements.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of items to skip.


## -returns



Type: <b>HRESULT</b>

Return S_OK if the method succeeds.



