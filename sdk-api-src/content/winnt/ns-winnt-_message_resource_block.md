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

# _MESSAGE_RESOURCE_BLOCK structure


## -description


Contains information about message strings with identifiers in the range indicated by the 
			<b>LowId</b> and 
			<b>HighId</b> members. 


## -struct-fields




### -field LowId

Type: <b>DWORD</b>

The lowest message identifier contained within this structure. 


### -field HighId

Type: <b>DWORD</b>

The highest message identifier contained within this structure. 


### -field OffsetToEntries

Type: <b>DWORD</b>

The offset, in bytes, from the beginning of the <a href="https://msdn.microsoft.com/439cf64e-29be-49ab-8bbf-cb98ac2e41cd">MESSAGE_RESOURCE_DATA</a> structure to the <a href="https://msdn.microsoft.com/cce13b09-5c8b-4d64-a229-419d01d91f27">MESSAGE_RESOURCE_ENTRY</a> structures in this <b>MESSAGE_RESOURCE_BLOCK</b>. The <b>MESSAGE_RESOURCE_ENTRY</b> structures contain the message strings. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/439cf64e-29be-49ab-8bbf-cb98ac2e41cd">MESSAGE_RESOURCE_DATA</a>



<a href="https://msdn.microsoft.com/cce13b09-5c8b-4d64-a229-419d01d91f27">MESSAGE_RESOURCE_ENTRY</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

