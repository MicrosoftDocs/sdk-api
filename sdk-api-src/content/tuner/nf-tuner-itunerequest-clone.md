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

# ITuneRequest::Clone


## -description



The <b>Clone</b> method returns a new copy of this tune request.




## -parameters




### -param NewTuneRequest






#### - ppNewTuneRequest [out]

Address of an <b>ITuneRequest</b> interface pointer that will be set to the new object.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method performs a "deep copy" of the object; in other words it copies all sub-objects as well, including <a href="https://msdn.microsoft.com/library/windows/hardware/dn922646">Components</a>, <a href="https://msdn.microsoft.com/d1601651-84a2-4fd8-9318-653aa569e747">LanguageComponentType</a> objects, and so on.




## -see-also




<a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest Interface</a>
 

 

