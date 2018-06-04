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

# MBN_SMS_STATUS_INFO structure


## -description


The <b>MBN_SMS_STATUS_INFO</b> structure contains the status of the SMS message store of a device.


## -struct-fields




### -field flag

A bitwise OR combination of <a href="https://msdn.microsoft.com/835cfdfa-face-4779-8bbf-e35076b85521">MBN_SMS_STATUS_FLAG</a> values that specify the state of the message store.


### -field messageIndex

Contains the index of the last received message in the store.  This field is only meaningful when <b>flag</b> contains <b>MBN_SMS_FLAG_NEW_MESSAGE</b>.

