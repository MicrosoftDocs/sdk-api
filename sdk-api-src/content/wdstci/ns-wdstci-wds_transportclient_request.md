---
UID: NS:wdstci._WDS_TRANSPORTCLIENT_REQUEST
title: WDS_TRANSPORTCLIENT_REQUEST (wdstci.h)
description: This structure is used by the WdsTransportClientStartSession function.
helpviewer_keywords: ["*PWDS_TRANSPORTCLIENT_REQUEST","PWDS_TRANSPORTCLIENT_REQUEST","PWDS_TRANSPORTCLIENT_REQUEST structure pointer [Windows Deployment Services]","WDS_TRANSPORTCLIENT_AUTH","WDS_TRANSPORTCLIENT_NO_AUTH","WDS_TRANSPORTCLIENT_PROTOCOL_MULTICAST","WDS_TRANSPORTCLIENT_REQUEST","WDS_TRANSPORTCLIENT_REQUEST structure [Windows Deployment Services]","WDS_TRANSPORT_CLIENT_CURRENT_API_VERSION","wds.wds_transportclient_request","wdstci/PWDS_TRANSPORTCLIENT_REQUEST","wdstci/WDS_TRANSPORTCLIENT_REQUEST"]
old-location: wds\wds_transportclient_request.htm
tech.root: wds
ms.assetid: efa1ea12-5234-474b-a859-cd074290e375
ms.date: 12/05/2018
ms.keywords: '*PWDS_TRANSPORTCLIENT_REQUEST, PWDS_TRANSPORTCLIENT_REQUEST, PWDS_TRANSPORTCLIENT_REQUEST structure pointer [Windows Deployment Services], WDS_TRANSPORTCLIENT_AUTH, WDS_TRANSPORTCLIENT_NO_AUTH, WDS_TRANSPORTCLIENT_PROTOCOL_MULTICAST, WDS_TRANSPORTCLIENT_REQUEST, WDS_TRANSPORTCLIENT_REQUEST structure [Windows Deployment Services], WDS_TRANSPORT_CLIENT_CURRENT_API_VERSION, wds.wds_transportclient_request, wdstci/PWDS_TRANSPORTCLIENT_REQUEST, wdstci/WDS_TRANSPORTCLIENT_REQUEST'
req.header: wdstci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WDS_TRANSPORTCLIENT_REQUEST, *PWDS_TRANSPORTCLIENT_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WDS_TRANSPORTCLIENT_REQUEST
 - wdstci/_WDS_TRANSPORTCLIENT_REQUEST
 - PWDS_TRANSPORTCLIENT_REQUEST
 - wdstci/PWDS_TRANSPORTCLIENT_REQUEST
 - WDS_TRANSPORTCLIENT_REQUEST
 - wdstci/WDS_TRANSPORTCLIENT_REQUEST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstci.h
api_name:
 - WDS_TRANSPORTCLIENT_REQUEST
---

# WDS_TRANSPORTCLIENT_REQUEST structure


## -description

This structure is used by the <a href="/windows/desktop/api/wdstci/nf-wdstci-wdstransportclientstartsession">WdsTransportClientStartSession</a> function.

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