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

# IPersistStreamInit::GetSizeMax


## -description


Retrieves the size of the stream needed to save the object.


## -parameters




### -param pCbSize [out]

The size in bytes of the stream needed to save this object, in bytes.


## -returns



This method returns S_OK to indicate that the size was retrieved successfully.




## -remarks



This method returns the size needed to save an object. You can call this method to determine the size and set the necessary buffers before calling the <a href="https://msdn.microsoft.com/f88b61d0-dd85-4e8e-b445-dfced6521981">IPersistStreamInit::Save</a> method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The <b>GetSizeMax</b> implementation should return a conservative estimate of the necessary size because the caller might call the <a href="https://msdn.microsoft.com/f88b61d0-dd85-4e8e-b445-dfced6521981">IPersistStreamInit::Save</a> method with a non-growable stream.




## -see-also




<a href="https://msdn.microsoft.com/49c413b3-3523-4602-9ec1-19f4e0fe5651">IPersistStreamInit</a>
 

 

