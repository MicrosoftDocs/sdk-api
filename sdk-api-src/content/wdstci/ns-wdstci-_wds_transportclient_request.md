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

# _WDS_TRANSPORTCLIENT_REQUEST structure


## -description


This structure is used by the <a href="https://msdn.microsoft.com/aa89899f-8f50-4617-84a1-4013412f0292">WdsTransportClientStartSession</a> function.


## -struct-fields




### -field ulLength

The length of this structure in bytes.


### -field ulApiVersion

The version of the API that the caller is built against.  The multicast client may reject the request based on this value.


This member must contain the following value.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WDS_TRANSPORT_CLIENT_CURRENT_API_VERSION"></a><a id="wds_transport_client_current_api_version"></a><dl>
<dt><b>WDS_TRANSPORT_CLIENT_CURRENT_API_VERSION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The current version.

</td>
</tr>
</table>
 


### -field ulAuthLevel

This member can contain one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WDS_TRANSPORTCLIENT_AUTH"></a><a id="wds_transportclient_auth"></a><dl>
<dt><b>WDS_TRANSPORTCLIENT_AUTH</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Authentication information about this user will be sent to the server.  The server will use this information to determine if the user has access to this file.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_TRANSPORTCLIENT_NO_AUTH"></a><a id="wds_transportclient_no_auth"></a><dl>
<dt><b>WDS_TRANSPORTCLIENT_NO_AUTH</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
No authentication information will be sent to the server.  If the server is not configured to accept these requests, the request will fail.

</td>
</tr>
</table>
 


### -field pwszServer

Server name.


### -field pwszNamespace

Namespace of the object to retrieve.


### -field pwszObjectName

Specifies the name of the object to retrieve.  Object names are
     provider dependent.


### -field ulCacheSize

Specifies how much data in bytes the consumer can store in its queue.  Once
     this threshold is reached, the client will not send any more writes to
    the consumer until some memory is released with 
    WdsTransportClientCompleteWrite.


### -field ulProtocol

Specifies the protocol to be used for this transfer.


This member can contain the following value.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WDS_TRANSPORTCLIENT_PROTOCOL_MULTICAST"></a><a id="wds_transportclient_protocol_multicast"></a><dl>
<dt><b>WDS_TRANSPORTCLIENT_PROTOCOL_MULTICAST</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The file will be transferred using an efficient multicast protocol.

</td>
</tr>
</table>
 


### -field pvProtocolData

Protocol data structure for the protocol. The structure is <b>NULL</b> for  <b>WDS_TRANSPORTCLIENT_PROTOCOL_MULTICAST</b> protocol.


### -field ulProtocolDataLength

The length of the protocol data pointed to by <b>pvProtocolData</b>.

