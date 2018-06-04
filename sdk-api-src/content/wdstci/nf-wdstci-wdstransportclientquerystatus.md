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

# WdsTransportClientQueryStatus function


## -description


Retrieves the current status of an ongoing or complete multicast transmission from the multicast client.


## -parameters




### -param hSessionKey [in]

Unique handle returned by the call to <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a>.


### -param puStatus [out]

The current status of the transfer.  This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_STATUS_IN_PROGRESS</dt>
</dl>
</td>
<td width="60%">
The multicast session is still in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_STATUS_SUCCESS</dt>
</dl>
</td>
<td width="60%">
The multicast session completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_STATUS_FAILURE</dt>
</dl>
</td>
<td width="60%">
The multicast session failed.

</td>
</tr>
</table>
 


### -param puErrorCode [out]

If puStatus is set to <b>WDS_TRANSPORTCLIENT_STATUS_FAILURE</b>, this field will be set to the error code of the session.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



It is valid to call this function even after a transfer completes as long as the session key has not been closed.



