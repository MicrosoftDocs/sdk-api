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

# _DNS_WIRE_QUESTION structure


## -description


The <b>DNS_WIRE_QUESTION</b> structure contains information about a DNS question transmitted across the network as specified in section 4.1.2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=90264">RFC 1035</a>..


## -struct-fields




### -field QuestionType

A value that represents the question section's <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Question Type</a>.


### -field QuestionClass

A value that represents the question section's <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Question Class</a>.


## -remarks



When constructing a DNS message, the question name must precede the <b>DNS_WIRE_QUESTION</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/fb36930c-dd43-427a-8034-078c99497a3e">DNS_WIRE_RECORD</a>
 

 

