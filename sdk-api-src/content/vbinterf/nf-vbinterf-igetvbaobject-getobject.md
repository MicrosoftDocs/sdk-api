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

# IGetVBAObject::GetObject


## -description


Gets a pointer to an interface on the VBA object.
<div class="alert"><b>Note</b>  The use of this method is no longer recommended because containers other than Visual Basic do not support 
    it.</div><div> </div>

## -parameters




### -param riid [in]

Specifies the interface to retrieve. Pass <b>IID_IVBFormat</b> to retrieve a pointer to 
      the <a href="https://msdn.microsoft.com/6b05c0c7-6f38-42cf-bf7b-2a54a4302b68">IVBFormat</a> interface.


### -param ppvObj [out]

Pointer to the interface.


### -param dwReserved [in]

Reserved.


## -returns



This method supports the standard return values <b>E_INVALIDARG</b>, 
      <b>E_OUTOFMEMORY</b>, and <b>E_UNEXPECTED</b>, as well as the 
      following:




## -see-also




<a href="https://msdn.microsoft.com/dda96834-7fc9-4361-9861-b9831fc7e6fe">IGetVBAObject</a>
 

 

