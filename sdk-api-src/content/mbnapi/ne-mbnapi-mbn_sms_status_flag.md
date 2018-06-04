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

# MBN_SMS_STATUS_FLAG enumeration


## -description


The <b>MBN_SMS_STATUS_FLAG</b> enumerated type indicates the status of  a device's SMS message store.

These enumerated values are used in a bitfield by the <a href="https://msdn.microsoft.com/9146d230-c96c-4d70-9bc5-e91896e19d35">MBN_SMS_STATUS_INFO</a> structure.


## -enum-fields




### -field MBN_SMS_FLAG_NONE

There is no SMS status information to report.


### -field MBN_SMS_FLAG_MESSAGE_STORE_FULL

The message store is full.


### -field MBN_SMS_FLAG_NEW_MESSAGE

A new non-class 0 message has been received by the interface.

