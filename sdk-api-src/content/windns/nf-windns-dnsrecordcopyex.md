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

# DnsRecordCopyEx function


## -description


The 
<b>DnsRecordCopyEx</b> function creates a copy of a specified <a href="https://msdn.microsoft.com/675287c2-9394-4d32-8ef4-9bb64794d326">resource record</a> (RR). The 
<b>DnsRecordCopyEx</b> function is also capable of converting the character encoding during the copy operation.


## -parameters




### -param pRecord [in]

A pointer to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the RR to be copied.


### -param CharSetIn [in]

A <a href="https://msdn.microsoft.com/2674a4e5-c3e2-4a25-bd6f-1fc6b4db3012">DNS_CHARSET</a> value that specifies the character encoding of the source RR.


### -param CharSetOut [in]

A <a href="https://msdn.microsoft.com/2674a4e5-c3e2-4a25-bd6f-1fc6b4db3012">DNS_CHARSET</a> value that specifies the character encoding required of the destination record.


## -returns



Successful execution returns a pointer to the (newly created) destination record. Otherwise, returns null.




## -remarks



The <i>CharSetIn</i> parameter is used only if the character encoding of the source RR is not specified in <i>pRecord</i>.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/bdf9d6b4-b9d7-4886-8ea6-1e1f4dbcc99a">DnsRecordSetCopyEx</a>
 

 

