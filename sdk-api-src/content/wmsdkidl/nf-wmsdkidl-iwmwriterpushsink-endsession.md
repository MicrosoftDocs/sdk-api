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

# IWMWriterPushSink::EndSession


## -description



The <b>EndSession</b> method ends the push distribution session. This method sends an end-of-stream message to the server, and then shuts down the data path on the server.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_CONNECTION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
A connection failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
There is no connection to the server. (Possibly this method was called before any connection was made.)

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/47bee154-0d29-4f4c-ac38-af8747088024">IWMWriterPushSink Interface</a>
 

 

