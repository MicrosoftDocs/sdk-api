---
UID: NF:mbnapi.IMbnVendorSpecificEvents.OnSetVendorSpecificComplete
title: IMbnVendorSpecificEvents::OnSetVendorSpecificComplete
author: windows-sdk-content
description: Notification method indicating that a vendor-specific operation has completed.
old-location: mbn\imbnvendorspecificevents_onsetvendorspecificcomplete.htm
old-project: mbn
ms.assetid: fc45b203-3e8e-436c-a554-164634026ecc
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IMbnVendorSpecificEvents interface [Microsoft Broadband Networks],OnSetVendorSpecificComplete method, IMbnVendorSpecificEvents.OnSetVendorSpecificComplete, IMbnVendorSpecificEvents::OnSetVendorSpecificComplete, OnSetVendorSpecificComplete, OnSetVendorSpecificComplete method [Microsoft Broadband Networks], OnSetVendorSpecificComplete method [Microsoft Broadband Networks],IMbnVendorSpecificEvents interface, mbn.imbnvendorspecificevents_onsetvendorspecificcomplete, mbnapi/IMbnVendorSpecificEvents::OnSetVendorSpecificComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnVendorSpecificEvents.OnSetVendorSpecificComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnVendorSpecificEvents::OnSetVendorSpecificComplete


## -description


Notification method indicating that a vendor-specific operation has completed.


## -parameters




### -param vendorOperation [in]

An <a href="https://msdn.microsoft.com/cbc905f6-c5ac-4c6a-9021-4ec00b938bb2">IMbnVendorSpecificOperation</a> interface representing the operation that completed.


### -param vendorSpecificData [in]

A byte array containing the data returned by underlying miniport driver. 


### -param requestID [in]

A request ID assigned by the Mobile Broadband service to identify the vendor-specific operation request.


## -returns



This method must return <b>S_OK</b>.




## -remarks



This byte array contains the byte by byte copy of data returned by underlying miniport driver. The Mobile Broadband service will free the memory for this field after the function call returns. If an application wants to use this data then it should copy the contents in its own memory.




## -see-also




<a href="https://msdn.microsoft.com/28507e68-5eaa-4b9d-bbb4-e276f4c213d5">IMbnVendorSpecificEvents</a>
 

 

