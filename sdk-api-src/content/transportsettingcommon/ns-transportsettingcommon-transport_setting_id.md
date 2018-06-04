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

# TRANSPORT_SETTING_ID structure


## -description


The <b>TRANSPORT_SETTING_ID</b> structure specifies the transport setting ID used by the  <a href="https://msdn.microsoft.com/FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715">SIO_APPLY_TRANSPORT_SETTING</a> and <a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a> IOCTLs to apply or query the transport setting for a socket.


## -struct-fields




### -field Guid

The transport setting ID. 


## -remarks



The only transport setting defined for Windows 8 and Windows Server 2012 is for the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> capability on a TCP socket. For Windows 10 and Windows Server 2016, there is another transport setting defined as <b>ASSOCIATE_NAMERES_CONTEXT</b>.

The <b>TRANSPORT_SETTING_ID</b> structure is passed as input to the <a href="https://msdn.microsoft.com/FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715">SIO_APPLY_TRANSPORT_SETTING</a> and <a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a> 
        IOCTLs. The <b>Guid</b> member determines what transport setting is applied or queried. 

The only transport setting currently defines is for the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> capability on a TCP socket.




## -see-also




<a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a>



<a href="https://msdn.microsoft.com/A008310D-D812-4DCD-A3F2-64FEEEB31DB8">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a>



<a href="https://msdn.microsoft.com/FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715">SIO_APPLY_TRANSPORT_SETTING</a>



<a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a>
 

 

