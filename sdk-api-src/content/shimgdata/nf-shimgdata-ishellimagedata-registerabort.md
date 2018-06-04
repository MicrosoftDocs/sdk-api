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

# IShellImageData::RegisterAbort


## -description


Sets a callback abort object, optionally returning a pointer to the previous object.


## -parameters




### -param pAbort [in]

Type: <b><a href="https://msdn.microsoft.com/98a79c41-a384-4486-af51-a33cd5f0750e">IShellImageDataAbort</a>*</b>

A pointer to an abort object. If this parameter is <b>NULL</b>, an unhandled exception results.


### -param ppAbortPrev [out, optional]

Type: <b><a href="https://msdn.microsoft.com/98a79c41-a384-4486-af51-a33cd5f0750e">IShellImageDataAbort</a>**</b>

The address of a pointer to the previous abort object. This parameter can be <b>NULL</b> if the previous object is not of interest.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful or an error value otherwise.



