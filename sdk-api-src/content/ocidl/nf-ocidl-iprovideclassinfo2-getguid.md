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

# IProvideClassInfo2::GetGUID


## -description


Retrieves the specified GUID for the object.


## -parameters




### -param dwGuidKind [in]

The GUID type. Possible values are from the <a href="https://msdn.microsoft.com/b9ddd96b-0418-4e31-aaf9-ca060c405fa7">GUIDKIND</a> enumeration.


### -param pGUID [out]

A pointer to a variable that receives the GUID.


## -returns



This method can return the standard return values E_INVALIDARG, E_UNEXPECTED, E_POINTER, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/e62785e4-994c-48cc-b5b9-7ec2b07c9d63">IProvideClassInfo2</a>
 

 

