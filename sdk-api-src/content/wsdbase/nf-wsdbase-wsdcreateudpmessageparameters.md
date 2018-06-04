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

# WSDCreateUdpMessageParameters function


## -description


Retrieves a pointer to the <a href="https://msdn.microsoft.com/3af6e0ff-c0b9-47af-b018-37567f614adc">IWSDUdpMessageParameters</a> interface.


## -parameters




### -param ppTxParams [out]

Pointer to the <a href="https://msdn.microsoft.com/3af6e0ff-c0b9-47af-b018-37567f614adc">IWSDUdpMessageParameters</a> interface that you use to specify how often WSD repeats the message transmission.


## -returns



Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppTxParams</i> is <b>NULL</b>.

</td>
</tr>
</table>
 



