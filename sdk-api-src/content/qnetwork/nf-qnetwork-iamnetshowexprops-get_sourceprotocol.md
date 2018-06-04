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

# IAMNetShowExProps::get_SourceProtocol


## -description



The <code>get_SourceProtocol</code> method retrieves the source protocol.




## -parameters




### -param pSourceProtocol

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Unknown protocol</td>
</tr>
<tr>
<td>1</td>
<td>Multicast</td>
</tr>
<tr>
<td>2</td>
<td>Multisession bridge</td>
</tr>
<tr>
<td>3</td>
<td>UDP</td>
</tr>
<tr>
<td>4</td>
<td>TCP</td>
</tr>
<tr>
<td>5</td>
<td>Media Streaming Broadcast Distribution (MSBD)</td>
</tr>
<tr>
<td>6</td>
<td>HTTP</td>
</tr>
<tr>
<td>7</td>
<td>File</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e68959dc-1a79-4e2c-aeaf-3febcb9c09ce">IAMNetShowExProps Interface</a>
 

 

