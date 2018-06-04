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

# _BLUETOOTH_OOB_DATA_INFO structure


## -description


The <b>BLUETOOTH_OOB_DATA_INFO</b> structure contains data used to authenticate prior to establishing an Out-of-Band device pairing.


## -struct-fields




### -field C

A 128-bit cryptographic key used for two-way authentication.


### -field R

A randomly generated number used for one-way authentication. If this number is not provided by the device initiating the OOB session, this value is 0.


## -remarks



For more details regarding the creation of keys for OOB authentication, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=178090">Bluetooth Core Specification</a>.



