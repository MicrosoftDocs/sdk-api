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

# IWbemContext::Clone


## -description


The 
<b>IWbemContext::Clone</b> method makes a logical copy of the current 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object. This method can be useful when many calls must be made which have largely identical 
<b>IWbemContext</b> objects.


## -parameters




### -param ppNewCopy [out]

Must point to <b>NULL</b> on entry. It receives a pointer to the new object containing the clone of the current object. The returned pointer has a positive reference count. The caller must call <b>IWbemServices::Release</b> on this pointer when it is no longer needed. On error, this pointer is left unmodified, and a new object is not returned.


## -returns



This method returns an <b>HRESULT</b>HRESULT indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>HRESULT.



