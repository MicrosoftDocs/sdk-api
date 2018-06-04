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

# IMbnVendorSpecificOperation::SetVendorSpecific


## -description


Sends a request to the underlying Mobile Broadband device miniport driver.


## -parameters




### -param vendorSpecificData [in]

A byte array that is passed in to the miniport driver. 


### -param requestID [out]

A unique request ID assigned by the Mobile Broadband service to identify this request.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>SetVendorSpecific</b> exists to implement vendor-specific functionality which is not otherwise covered in the Mobile Broadband API.

The Mobile Broadband service will issue a SET OID request to the underlying miniport driver for OID_WWAN_VENDOR_SPECIFIC OID.  <i>VendorspecificData</i> will be copied byte by byte into the data buffer passed in the OID request.

This is an asynchronous operation and <b>SetVendorSpecific</b> will return immediately.  On completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/fc45b203-3e8e-436c-a554-164634026ecc">OnSetVendorSpecificComplete</a> method of the  <a href="https://msdn.microsoft.com/28507e68-5eaa-4b9d-bbb4-e276f4c213d5">IMbnVendorSpecificEvents</a> interface.

Refer to  the Mobile Broadband Driver Model for more information about vendor specific operations.





## -see-also




<a href="https://msdn.microsoft.com/cbc905f6-c5ac-4c6a-9021-4ec00b938bb2">IMbnVendorSpecificOperation</a>
 

 

