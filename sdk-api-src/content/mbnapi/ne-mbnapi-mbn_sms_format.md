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

# MBN_SMS_FORMAT enumeration


## -description


The <b>MBN_SMS_FORMAT</b> enumerated type specifies the format of SMS messages. 


## -enum-fields




### -field MBN_SMS_FORMAT_NONE

No SMS format.


### -field MBN_SMS_FORMAT_PDU

For GSM devices, SMS, messages will be read in PDU format. 

For CDMA devices, SMS messages will be read in binary CDMA format.


### -field MBN_SMS_FORMAT_TEXT

For CDMA devices, SMS messages will be read in text format.

