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

# MBN_SMS_FILTER structure


## -description


The <b>MBN_SMS_FILTER</b> structure contains the values that describe a set of SMS messages.


## -struct-fields




### -field flag

An <a href="https://msdn.microsoft.com/caabe2b2-86f0-40e7-b5ee-aeda8b64651a">MBN_SMS_FLAG</a> value that 	specifies the message class.


### -field messageIndex

Contains the index of a particular message in device memory.  This value is only meaningful when <b>flag</b> is set to 	<b>MBN_SMS_FLAG_INDEX</b>.  The maximum range of this value is from 1 to the <a href="https://msdn.microsoft.com/c7dee4b7-4a34-4d08-aae3-7455531a9556">MaxMessageIndex</a> property of <a href="https://msdn.microsoft.com/ee261c32-aa17-496a-a568-d9da43e1e23a">IMbnSmsConfiguration</a>. 

