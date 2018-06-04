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

# GetHGlobalFromILockBytes function


## -description



			The 
<b>GetHGlobalFromILockBytes</b> function retrieves a global memory handle to a byte array object created using the 
<a href="https://msdn.microsoft.com/e7963be7-ccd8-49fb-85bb-e22fbbb6dc5c">CreateILockBytesOnHGlobal</a> function.


## -parameters




### -param plkbyt

TBD


### -param phglobal [out]

Pointer to the current memory handle used by the specified byte-array object.


#### - pLkbyt [in]

Pointer to the 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface on the byte-array object previously created by a call to the 
<a href="https://msdn.microsoft.com/e7963be7-ccd8-49fb-85bb-e22fbbb6dc5c">CreateILockBytesOnHGlobal</a> function.


## -returns



This function returns HRESULT.




## -remarks



After a call to 
<a href="https://msdn.microsoft.com/e7963be7-ccd8-49fb-85bb-e22fbbb6dc5c">CreateILockBytesOnHGlobal</a>, which creates a byte array object on global memory, 
<b>GetHGlobalFromILockBytes</b> retrieves a pointer to the handle of the global memory underlying the byte array object. The handle this function returns might be different from the original handle due to intervening calls to the <a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> function.

The contents of the returned memory handle can be written to a clean disk file, and then opened as a storage object using the 
<a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a> function.

This function only works within the same process from which the byte array was created.




## -see-also




<a href="https://msdn.microsoft.com/e7963be7-ccd8-49fb-85bb-e22fbbb6dc5c">CreateILockBytesOnHGlobal</a>



<a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a>
 

 

