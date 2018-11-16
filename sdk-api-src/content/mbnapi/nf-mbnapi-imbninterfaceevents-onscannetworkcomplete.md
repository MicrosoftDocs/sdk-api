---
UID: NF:mbnapi.IMbnInterfaceEvents.OnScanNetworkComplete
title: IMbnInterfaceEvents::OnScanNetworkComplete
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate the completion of a network scan.
old-location: mbn\imbninterfaceevents_onscannetworkcomplete.htm
tech.root: mbn
ms.assetid: 6320c76b-b8a6-44dc-88bb-e20a85d5cfca
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: E_MBN_ALREADY_ACTIVE, E_MBN_DEVICE_BUSY, E_MBN_RADIO_POWER_OFF, IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnScanNetworkComplete method, IMbnInterfaceEvents.OnScanNetworkComplete, IMbnInterfaceEvents::OnScanNetworkComplete, OnScanNetworkComplete, OnScanNetworkComplete method [Microsoft Broadband Networks], OnScanNetworkComplete method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, S_OK, mbn.imbninterfaceevents_onscannetworkcomplete, mbnapi/IMbnInterfaceEvents::OnScanNetworkComplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnInterfaceEvents.OnScanNetworkComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mbnapi.h
: 
- IMbnInterfaceEvents.OnScanNetworkComplete
: 
---

# IMbnInterfaceEvents::OnScanNetworkComplete


## -description


This notification method is called by the Mobile Broadband service to indicate the completion of a network scan.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> that represents a device on which this operation was performed.


### -param requestID [in]

The request ID assigned by the Mobile Broadband service for this notification.


### -param status [in]

The operation completion status

.

A calling application can expect one of the following values.



##### )



###### )



###### )



##### )


## -returns



This method must return <b>S_OK</b>.




## -remarks



If the operation completed successfully, that is, when <i>status</i> is  S_OK,  the Mobile Broadband service successfully updated the cached list of visible providers.  An application can then call the <a href="https://msdn.microsoft.com/916c29ee-adb3-402c-b4f3-97b8977f44ac">GetVisibleProviders</a> method of the passed <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> to get the list of visible providers.

If multiple applications registered for notifications, then this method will be called on all registered applications. This means that an application that did not initiate the update operation will receive a notification.




## -see-also




<a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>
 

 

