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

# IGlobalOptions::Set


## -description


Sets the specified global property of the COM runtime.


## -parameters




### -param dwProperty [in]

 The global property of the COM runtime. For a list of properties that can be set with this method, see <a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a>.


### -param dwValue [in]

The value of the property.<div class="alert"><b>Important</b>  For the COMGLB_APPID property, this parameter must specify a pointer to the APPID GUID.</div>
<div> </div>



## -returns



The return value is S_OK if the property was set successfully.




## -see-also




<a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a>
 

 

