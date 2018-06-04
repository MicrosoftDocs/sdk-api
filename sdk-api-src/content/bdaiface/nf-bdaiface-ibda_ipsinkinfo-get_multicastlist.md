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

# IBDA_IPSinkInfo::get_MulticastList


## -description



This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        



The <b>get_MulticastList</b> method retrieves a list of the multicast addresses to which the IP Sink filter is listening. This method returns a list of IP addresses in 6-byte IEEE 802.3 format; the list is returned as an array of bytes.


## -parameters




### -param pulcbAddresses [out]

Receives the number of bytes in the returned array.


### -param ppbAddressList [out]

Pointer to variable that receives an array of bytes, of size *<i>pulcbAddresses</i>. Each IP address is 6 consecutive bytes.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The method allocates the memory for the array. The caller must free the memory by calling <b>CoTaskMemFree</b>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/fbbe12ea-964a-4a83-ac0a-ac8808bd9a63">IBDA_IPSinkInfo Interface</a>
 

 

