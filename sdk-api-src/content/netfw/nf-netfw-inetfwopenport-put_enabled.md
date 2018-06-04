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

# INetFwOpenPort::put_Enabled


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the settings for this port are currently enabled.

This property is read/write.


## -parameters


## -remarks



This property can be set to false (<b>VARIANT_FALSE</b>) to allow port settings to be stored in the <a href="https://msdn.microsoft.com/a3a6e5c1-5818-419c-8df4-966b2fbcd8c0">INetFWOpenPorts</a> collection without actually opening the port. 

The default value is true (<b>VARIANT_TRUE</b>) for new ports.




## -see-also




<a href="https://msdn.microsoft.com/a3a6e5c1-5818-419c-8df4-966b2fbcd8c0">INetFWOpenPorts</a>



<a href="https://msdn.microsoft.com/1a9fd676-b1c0-4be5-9571-d14ac5980af5">INetFwOpenPort</a>
 

 

