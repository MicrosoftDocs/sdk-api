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

# IEnumExtraSearch::Next


## -description


Used to request information on one or more search objects.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of search objects to be enumerated, starting from the current object. If <i>celt</i> is too large, the method should stop and return the actual number of search objects in <i>pceltFetched</i>.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/d930a00b-3084-4da7-8915-0bebdb33df9b">EXTRASEARCH</a>*</b>

A pointer to an array of <i>pceltFetched</i> <a href="https://msdn.microsoft.com/d930a00b-3084-4da7-8915-0bebdb33df9b">EXTRASEARCH</a> structures containing information on the enumerated objects.


### -param pceltFetched [out]

Type: <b>ULONG*</b>


          The number of objects actually enumerated. This may be less than <i>celt</i>.
        


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.



