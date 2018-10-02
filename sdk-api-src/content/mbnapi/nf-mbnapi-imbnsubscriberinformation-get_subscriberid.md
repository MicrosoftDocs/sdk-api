---
UID: NF:mbnapi.IMbnSubscriberInformation.get_SubscriberID
title: IMbnSubscriberInformation::get_SubscriberID
author: windows-sdk-content
description: The subscriber ID of the device.
old-location: mbn\imbnsubscriberinformation_subscriberid.htm
tech.root: mbn
ms.assetid: 5ea22495-44b3-4b2b-8c7a-a012f9c99387
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMbnSubscriberInformation interface [Microsoft Broadband Networks],SubscriberID property, IMbnSubscriberInformation.SubscriberID, IMbnSubscriberInformation.get_SubscriberID, IMbnSubscriberInformation::SubscriberID, IMbnSubscriberInformation::get_SubscriberID, SubscriberID property [Microsoft Broadband Networks], SubscriberID property [Microsoft Broadband Networks],IMbnSubscriberInformation interface, get_SubscriberID, mbn.imbnsubscriberinformation_subscriberid, mbnapi/IMbnSubscriberInformation::SubscriberID, mbnapi/IMbnSubscriberInformation::get_SubscriberID
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMbnSubscriberInformation.SubscriberID
 - IMbnSubscriberInformation.get_SubscriberID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnSubscriberInformation::get_SubscriberID


## -description


The subscriber ID of the device.

This property is read-only.


## -parameters


## -remarks



This is a null terminated string of digits. For GSM device this represents the International Mobile Equipment Identity (IMSI) string (up to 15 digits). For CDMA device this represents the Mobile Identification Number (MIN) string or the International Roaming MIN (IRM) string (10 digits). 

Normally, this value is available only when the ready state of the device is <b>MBN_READY_STATE_INITIALIZED</b> In some cases, it may be populated in other states such as <b>MBN_READY_STATE_DEVICE_LOCKED</b>, <b>MBN_READY_STATE_BAD_SIM</b>,  and <b>MBN_READY_STATE_FAILURE</b>. When this information is not available it is returned as an empty string "".




## -see-also




<a href="https://msdn.microsoft.com/ef7f5dc5-ed66-450c-9623-0c1d725d82c6">IMbnSubscriberInformation</a>
 

 

