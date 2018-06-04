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

# ITraceDataProvider::get_Properties


## -description


Retrieves the list of extended data items that Event Tracing for Windows (ETW) includes with the event.

This property is read-only.


## -parameters


## -remarks



Use this property to request the following data items with the event.

<table>
<tr>
<th>Data item</th>
<th>Description</th>
</tr>
<tr>
<td>
Sid (value 0x01)

</td>
<td>
Includes the user's security identifier.

</td>
</tr>
<tr>
<td>
SessionId (value 0x02)

</td>
<td>
Includes the session identifier.

</td>
</tr>
<tr>
<td>
StackTrace (value 0x04)

</td>
<td>
Includes the stack trace.

</td>
</tr>
</table>
 

Use the <a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a> interface to retrieve or specify the extended data items. The <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a> property contains items that are combined by using the <b>OR</b> operator. The <a href="https://msdn.microsoft.com/965a5ac4-a811-4fd3-8862-51d82d27c0e9">IValueMapItem::Key</a> property contains the string representation of the extended data item. The <a href="https://msdn.microsoft.com/3f7549aa-2ad6-40f4-ae09-c5130a9c3451">IValueMapItem::Value</a> property contains the extended data item value.




## -see-also




<a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">ITraceDataProvider</a>
 

 

