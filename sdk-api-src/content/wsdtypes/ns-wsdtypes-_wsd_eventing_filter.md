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

# _WSD_EVENTING_FILTER structure


## -description


Represents an event filter used in WS-Eventing Subscribe messages.


## -struct-fields




### -field Dialect

Specifies the language or dialect use to represent the boolean expression used by the filter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_Action"></a><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_action"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2006_02_DEVPROF_ACTION"></a><dl>
<dt><b>http://schemas.xmlsoap.org/ws/2006/02/devprof/Action</b></dt>
</dl>
</td>
<td width="60%">
The boolean expression uses the Action filter dialect.

</td>
</tr>
</table>
 


### -field FilterAction

 


### -field Data

A reference to the expression used for filtering.  

