---
UID: NF:mbnapi.IMbnSubscriberInformation.get_TelephoneNumbers
title: IMbnSubscriberInformation::get_TelephoneNumbers
author: windows-sdk-content
description: The telephone numbers associated with the device.
old-location: mbn\imbnsubscriberinformation_telephonenumbers.htm
old-project: mbn
ms.assetid: 0f50735e-e57b-4724-8754-1fc4a5634cb3
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnSubscriberInformation interface [Microsoft Broadband Networks],TelephoneNumbers property, IMbnSubscriberInformation.TelephoneNumbers, IMbnSubscriberInformation.get_TelephoneNumbers, IMbnSubscriberInformation::TelephoneNumbers, IMbnSubscriberInformation::get_TelephoneNumbers, TelephoneNumbers property [Microsoft Broadband Networks], TelephoneNumbers property [Microsoft Broadband Networks],IMbnSubscriberInformation interface, get_TelephoneNumbers, mbn.imbnsubscriberinformation_telephonenumbers, mbnapi/IMbnSubscriberInformation::TelephoneNumbers, mbnapi/IMbnSubscriberInformation::get_TelephoneNumbers
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
 - IMbnSubscriberInformation.TelephoneNumbers
 - IMbnSubscriberInformation.get_TelephoneNumbers
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSubscriberInformation::get_TelephoneNumbers


## -description


The telephone numbers associated with the device.

This property is read-only.


## -parameters


## -remarks



This property provides the list of telephone numbers (TNs) assigned to the subscriber. In GSM the numbers are called Mobile Station ISDN Numbers (MSISDNs).  In CDMA they are called Mobile Directory Numbers (MDNs).

This value is not populated until the ready state reaches <b>MBN_READY_STATE_INITIALIZED</b>.




## -see-also




<a href="https://msdn.microsoft.com/ef7f5dc5-ed66-450c-9623-0c1d725d82c6">IMbnSubscriberInformation</a>
 

 

