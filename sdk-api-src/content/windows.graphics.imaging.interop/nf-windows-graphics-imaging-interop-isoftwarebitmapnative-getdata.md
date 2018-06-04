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

# ISoftwareBitmapNative::imaging


## -description


This method returns an interface that provides access to the software bitmap data. 


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

The IID of the interface to retrieve.


### -param ppv

Type: <b>LPVOID*</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i> parameter.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK on successful completion. Returns E_NOINTERFACE if the requested interface can't be found.




## -see-also




<a href="https://msdn.microsoft.com/9EB9C74E-A056-4A40-AFAD-0056E139BA28">ISoftwareBitmapNative</a>
 

 

