---
UID: NF:mbnapi.IMbnSubscriberInformation.get_SimIccID
title: IMbnSubscriberInformation::get_SimIccID
author: windows-sdk-content
description: The SIM International circuit card number (SimICCID) for the device.
old-location: mbn\imbnsubscriberinformation_simiccid.htm
old-project: mbn
ms.assetid: 18132836-65e8-4372-bfcd-ba0115b2d4d0
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMbnSubscriberInformation interface [Microsoft Broadband Networks],SimIccID property, IMbnSubscriberInformation.SimIccID, IMbnSubscriberInformation.get_SimIccID, IMbnSubscriberInformation::SimIccID, IMbnSubscriberInformation::get_SimIccID, SimIccID property [Microsoft Broadband Networks], SimIccID property [Microsoft Broadband Networks],IMbnSubscriberInformation interface, get_SimIccID, mbn.imbnsubscriberinformation_simiccid, mbnapi/IMbnSubscriberInformation::SimIccID, mbnapi/IMbnSubscriberInformation::get_SimIccID
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
 - IMbnSubscriberInformation.SimIccID
 - IMbnSubscriberInformation.get_SimIccID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSubscriberInformation::get_SimIccID


## -description


The SIM International circuit card number (SimICCID) for the device.

This property is read-only.


## -parameters


## -remarks



The International Circuit Card Id of the SIM varies between 15 to 20 digits in length and is represented in characters. This value is available only when the ready state of the device is <b>MBN_READY_STATE_INITIALIZED</b>. In some cases, it may also be populated in states such as <b>MBN_READY_STATE_DEVICE_LOCKED</b>, <b>MBN_READY_STATE_BAD_SIM</b>,  and <b>MBN_READY_STATE_FAILURE</b>. When this information is not available it is returned as an empty string.




## -see-also




<a href="https://msdn.microsoft.com/ef7f5dc5-ed66-450c-9623-0c1d725d82c6">IMbnSubscriberInformation</a>
 

 

