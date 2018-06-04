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

# MBN_SMS_FLAG enumeration


## -description


The <b>MBN_SMS_FLAG</b> enumerated type specifies the SMS message class.

These enumerated values are used in the <a href="https://msdn.microsoft.com/f8dffd7b-3c12-43da-b61c-3c9aa8f1136f">MBN_SMS_FILTER</a> structure.


## -enum-fields




### -field MBN_SMS_FLAG_ALL

Refers to all the messages in the device message store.


### -field MBN_SMS_FLAG_INDEX

Refers to a single message in the device message store.


### -field MBN_SMS_FLAG_NEW

Refers to all new received and unread messages.


### -field MBN_SMS_FLAG_OLD

Refers to all old and read messages.


### -field MBN_SMS_FLAG_SENT

Refers to all sent and saved messages.


### -field MBN_SMS_FLAG_DRAFT

Refers to all unsent and saved messages.

