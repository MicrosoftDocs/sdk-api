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

# FaxExtInitializeConfig function


## -description


The fax service calls the <b>FaxExtInitializeConfig</b> function to initialize the fax extension DLL. The service calls this function before it calls any other fax extension initialization function.


## -parameters




### -param

TBD




#### - pFaxExtFreeBuffer [in]

Type: <b>PFAX_EXT_FREE_BUFFER</b>

Pointer to a <a href="https://msdn.microsoft.com/58a30203-b734-45fa-b502-6d97711f73e0">FaxExtFreeBuffer</a> fax service callback function.


#### - pFaxExtGetData [in]

Type: <b>PFAX_EXT_GET_DATA</b>

Pointer to a <a href="https://msdn.microsoft.com/164c3919-49ad-4d29-a44d-27985c877268">FaxExtGetData</a> fax service callback function.


#### - pFaxExtRegisterForEvents [in]

Type: <b>PFAX_EXT_REGISTER_FOR_EVENTS</b>

Pointer to a <a href="https://msdn.microsoft.com/a298f232-0670-4b0e-8962-4c111993dd36">FaxExtRegisterForEvents</a> fax service callback function.


#### - pFaxExtSetData [in]

Type: <b>PFAX_EXT_SET_DATA</b>

Pointer to a <a href="https://msdn.microsoft.com/e744ea8f-2b68-4a0a-b9ee-d83f10f078b2">FaxExtSetData</a> fax service callback function.


#### - pFaxExtUnregisterForEvents [in]

Type: <b>PFAX_EXT_UNREGISTER_FOR_EVENTS</b>

Pointer to a <a href="https://msdn.microsoft.com/7cab1f4c-7e2f-4510-af8a-f0aee81a044e">FaxExtUnregisterForEvents</a> fax service callback function.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, the return value is <b>NOERROR</b>.





If the fax extension DLL returns a value other than <b>NOERROR</b>, the fax service considers the extension to be in an error state. Even if other extension initialization functions succeed, the fax service does not recognize the extension.





## -remarks



A fax extension DLL must export <b>FaxExtInitializeConfig</b> if it plans to implement the fax extension configuration mechanism and receive notifications from the fax service about changes in device configuration data.

The <b>FaxExtInitializeConfig</b> function exposes pointers to the callback functions that the fax service supplies. The fax extension DLL must store these pointers in a global variable for later use.




## -see-also




<a href="https://msdn.microsoft.com/58a30203-b734-45fa-b502-6d97711f73e0">FaxExtFreeBuffer</a>



<a href="https://msdn.microsoft.com/164c3919-49ad-4d29-a44d-27985c877268">FaxExtGetData</a>



<a href="https://msdn.microsoft.com/a298f232-0670-4b0e-8962-4c111993dd36">FaxExtRegisterForEvents</a>



<a href="https://msdn.microsoft.com/e744ea8f-2b68-4a0a-b9ee-d83f10f078b2">FaxExtSetData</a>



<a href="https://msdn.microsoft.com/7cab1f4c-7e2f-4510-af8a-f0aee81a044e">FaxExtUnregisterForEvents</a>
 

 

