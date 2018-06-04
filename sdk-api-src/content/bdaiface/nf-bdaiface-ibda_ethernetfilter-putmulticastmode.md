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

# IBDA_EthernetFilter::PutMulticastMode


## -description



The <b>PutMulticastMode</b> method sets the multicast mode.




## -parameters




### -param ulModeMask [in]

Specifies the multicast mode.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



See the Windows DDK for possible values.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8a0a5dbb-642a-458b-a5b2-80e993ab61ca">GetMulticastMode</a>



<a href="https://msdn.microsoft.com/f4f9d6c0-0acf-416b-adb3-643ac0167d0a">IBDA_EthernetFilter Interface</a>
 

 

