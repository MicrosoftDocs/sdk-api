---
UID: NF:mbnapi.IMbnVendorSpecificEvents.OnEventNotification
title: IMbnVendorSpecificEvents::OnEventNotification
author: windows-sdk-content
description: Notification method signaling a change event from the underlying Mobile Broadband device miniport driver.
old-location: mbn\imbnvendorspecificevents_oneventnotification.htm
old-project: mbn
ms.assetid: c3d10e9c-b60f-42e8-adaa-2c0ba3c77718
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnVendorSpecificEvents interface [Microsoft Broadband Networks],OnEventNotification method, IMbnVendorSpecificEvents.OnEventNotification, IMbnVendorSpecificEvents::OnEventNotification, OnEventNotification, OnEventNotification method [Microsoft Broadband Networks], OnEventNotification method [Microsoft Broadband Networks],IMbnVendorSpecificEvents interface, mbn.imbnvendorspecificevents_oneventnotification, mbnapi/IMbnVendorSpecificEvents::OnEventNotification
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnVendorSpecificEvents.OnEventNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnVendorSpecificEvents::OnEventNotification


## -description


Notification method signaling a change event from the underlying Mobile Broadband device miniport driver.


## -parameters




### -param vendorOperation [in]

A <a href="https://msdn.microsoft.com/cbc905f6-c5ac-4c6a-9021-4ec00b938bb2">IMbnVendorSpecificOperation</a> interface representing the device on which the event has occurred.


### -param vendorSpecificData [in]

A byte array containing the data returned by underlying miniport driver. 


## -returns



This method must return <b>S_OK</b>.




## -remarks



This byte array contains the byte by byte copy of data returned by underlying miniport driver.  The Mobile Broadband service will free the memory for this field after the function call returns. If an application wants to use this data then it should copy the contents in its own memory.




## -see-also




<a href="https://msdn.microsoft.com/28507e68-5eaa-4b9d-bbb4-e276f4c213d5">IMbnVendorSpecificEvents</a>
 

 

