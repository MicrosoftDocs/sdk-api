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

# ITILSConfig::put_Port


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>put_Port</b> method sets the port number used to connect to the server of a specified ILS directory.


## -parameters




### -param Port [in]

The port number that will be used to connect to the server. This can be any port number in the range of 16-bit unsigned integers.


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>Port</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RND_ALREADY_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
A successful connection has been made. Port cannot be reset.

</td>
</tr>
</table>
 




## -remarks



Applications use this method only if they need to connect to custom-configured ILS servers listening on strange ports that are not listed in the Active Directory. By default, the Rendezvous control automatically tries to use ports 1002 and 389, the usual ILS ports, for connecting to application-specified ILS servers. Also, the Rendezvous control automatically uses whatever port is published in the Active Directory for ILS servers retrieved from there.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.




## -see-also




<a href="https://msdn.microsoft.com/92a5624b-acf5-4280-9932-860fde53c6a0">ITILSConfig</a>



<a href="https://msdn.microsoft.com/7aa0a8e7-6799-4685-92a0-c2ce610d0e06">ITILSConfig::get_Port</a>
 

 

