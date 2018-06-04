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

# ITravelLog::FindTravelEntry


## -description


Deprecated. Determines whether a specific travel entry is present in the travel log.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.


### -param pidl [in]

Type: <b>LPCITEMIDLIST</b>

A PIDL of the travel entry, typically obtained through <a href="https://msdn.microsoft.com/9a3a156f-4d61-4987-b1d8-9e77564d3962">GetPidl</a>.


### -param ppte [out]

Type: <b><a href="https://msdn.microsoft.com/b8a5d532-c1fd-4302-b983-cc9a74270321">ITravelEntry</a>**</b>

The address of a pointer to the <a href="https://msdn.microsoft.com/b8a5d532-c1fd-4302-b983-cc9a74270321">ITravelEntry</a> interface representing the travel entry, if found.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



