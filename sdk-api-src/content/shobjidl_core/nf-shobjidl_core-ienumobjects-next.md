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

# IEnumObjects::Next


## -description


Gets the next specified number and type of objects.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of objects to retrieve.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired interface ID.


### -param rgelt [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>.


### -param pceltFetched [out, optional]

Type: <b>ULONG*</b>

Pointer to a <b>ULONG</b> value that, when this method returns, states the actual number of objects retrieved. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the method successfully retrieved the requested objects. This method only returns S_OK if the full count of requested items are successfully retrieved.
                    
                    

S_FALSE indicates that more items were requested than remained in the enumeration.



