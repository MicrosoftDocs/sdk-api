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

# IWSDiscoveryPublisher::MatchProbe


## -description


Determines whether a <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> message matches the specified host and sends a WS-Discovery <a href="https://msdn.microsoft.com/58d3d016-ae29-4090-9b88-e1125db59c95">ProbeMatches</a> message if the match is made.


## -parameters




### -param pProbeMessage [in]

Pointer to a <a href="https://msdn.microsoft.com/e5352a78-3ece-45d3-bf95-2d922065e3d5">WSD_SOAP_MESSAGE</a> structure that represents the Probe message passed to the notification sink's <a href="https://msdn.microsoft.com/d92ce49c-308b-49e2-9646-f1eec2151441">ProbeHandler</a>.


### -param pMessageParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a> object that represents the transmission parameters passed in to the notification sink's <a href="https://msdn.microsoft.com/d92ce49c-308b-49e2-9646-f1eec2151441">ProbeHandler</a>.


### -param pszId [in]

The logical or physical address of the device, which is used as the device endpoint address. A logical address is of the form <code>urn:uuid:{guid}</code>. A physical address can be a URI prefixed by http or https, or simply a URI prefixed by <code>uri</code>. Whenever possible, use a logical address.


### -param ullMetadataVersion [in]

The current metadata version.

<div class="alert"><b>Note</b>  For compatibility with the <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery specification</a>, this value must be less than or equal to UINT_MAX (4294967295).</div>
<div> </div>

### -param ullInstanceId [in]

Identifier for the current instance of the device being published. This identifier must be incremented whenever the service is restarted.  For more information about instance identifiers, see Appendix I of the <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery specification</a>.

<div class="alert"><b>Note</b>  For compatibility with the <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery specification</a>, this value must be less than or equal to UINT_MAX (4294967295).</div>
<div> </div>

### -param ullMessageNumber [in]

Counter within the scope of the instance identifier for the current message. The message number must be incremented for each message.

<div class="alert"><b>Note</b>  For compatibility with the <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery specification</a>, this value must be less than or equal to UINT_MAX (4294967295).</div>
<div> </div>

### -param pszSessionId [in, optional]

Unique identifier within the scope of the instance identifier for the current session. This parameter corresponds to the sequence identifier in the AppSequence block in the Probe message. For more information about sequence identifiers, see Appendix I of the <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery specification</a>.

This parameter may be <b>NULL</b>.


### -param pTypesList [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/f573365d-100f-4df9-b1af-a484680436eb">WSD_NAME_LIST</a> structure that represents the list of types supported by the publishing host. May be <b>NULL</b>. 

If <i>pTypesList</i> is specified, <b>MatchProbe</b> will use WS-Discovery matching logic to verify that the types in the list match the types specified in <i>pProbeMessage</i>.


### -param pScopesList [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/86d77741-39c3-44bd-b072-d2d4eb99e488">WSD_URI_LIST</a> structure that represents the list of matching scopes supported by the publishing host. The list contains  hash values in string form. May be <b>NULL</b>.

If <i>pScopesList</i> is specified, <b>MatchProbe</b> will use WS-Discovery matching logic to verify that the scopes in the list match the scopes specified in <i>pProbeMessage</i>.


### -param pXAddrsList [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/86d77741-39c3-44bd-b072-d2d4eb99e488">WSD_URI_LIST</a> structure that represents the list of transport addresses supported by the publishing host. Each transport address string contains an address and port number which can be used for connection by a remote host. May be <b>NULL</b>.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the following conditions is true:

<ul>
<li><i>pszId</i> is <b>NULL</b>.</li>
<li>The length in characters of <i>pszId</i> exceeds WSD_MAX_TEXT_LENGTH (8192). </li>
<li>The length in characters of <i>pszSessionId</i> exceeds WSD_MAX_TEXT_LENGTH (8192). </li>
<li><i>pProbeMessage</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The publisher has not been started. Attaching a notification sink starts the publisher. To attach a sink, call <a href="https://msdn.microsoft.com/75a6c593-298b-45b4-bde5-2a383b7581cc">RegisterNotificationSink</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



<b>MatchProbe</b> should be called only when the discovery publisher has issued a <a href="https://msdn.microsoft.com/d92ce49c-308b-49e2-9646-f1eec2151441">ProbeHandler</a> callback. <i>pProbeMessage</i> and <i>pMessageParameters</i> are passed directly from the callback into <b>MatchProbe</b>. The <b>ProbeHandler</b> also passes information required by the publisher to determine if the supplied Probe message matches and, if so, to issue a ProbeMatches response if appropriate.

<b>MatchProbe</b> sends ProbeMatches messages on all bound adapters and automatically issues message retransmissions when required by WS-Discovery.




## -see-also




<a href="https://msdn.microsoft.com/4fff1328-d315-4a26-b7d8-43a273133e08">IWSDiscoveryPublisher</a>
 

 

