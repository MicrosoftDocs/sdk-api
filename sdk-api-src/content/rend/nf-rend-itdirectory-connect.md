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

# ITDirectory::Connect


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Connect</b> method establishes a connection to the directory server.
			


## -parameters




### -param fSecure [in]

Boolean indicator of whether to use SSL connection.


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
<dt><b>RND_ALREADY_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
A successful connection has already been made.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RND_NULL_SERVER_NAME</b></dt>
</dl>
</td>
<td width="60%">
The server name is <b>NULL</b>, probably because 
<a href="https://msdn.microsoft.com/ba492503-90ff-45dd-a39f-6d4451e57339">ITConferenceBlob::Init</a> has not been run or did not succeed.

</td>
</tr>
</table>
 




## -remarks



The 
<b>Connect</b> method must be successfully called before any other function except 
<a href="https://msdn.microsoft.com/3f0ca4c2-4ba9-4a6e-877b-36486086368f">get_DirectoryType</a>.




## -see-also




<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a>
 

 

