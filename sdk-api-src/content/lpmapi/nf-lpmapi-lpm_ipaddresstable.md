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

# LPM_IpAddressTable function


## -description


The 
<i>LPM_IpAddressTable</i> function is used by the PCM to pass a list of IP addresses assigned to the Windows 2000 Server upon which the LPM is initialized. The PCM calls this routine after the LPM has successfully initialized, but before making any requests. The PCM also uses the 
<i>LPM_IpAddressTable</i> function to update LPMs regarding IP address changes. LPMs are expected to detect IP address changes and update their states appropriately.


## -parameters




### -param cIpAddrTable [in]

Number of addresses in the IP table.


### -param pIpAddrTable [in]

Pointer to an 
<a href="https://msdn.microsoft.com/cbd67aa2-8b87-4e24-8a8e-a6c60cebf31f">LPMIPTABLE</a> structure that contains the IP addresses assigned to the Windows 2000 Server on which the LPM resides.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/cbd67aa2-8b87-4e24-8a8e-a6c60cebf31f">LPMIPTABLE</a>
 

 

