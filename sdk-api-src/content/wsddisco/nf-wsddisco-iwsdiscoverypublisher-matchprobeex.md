---
UID: NF:wsddisco.IWSDiscoveryPublisher.MatchProbeEx
title: IWSDiscoveryPublisher::MatchProbeEx (wsddisco.h)
author: windows-sdk-content
description: Determines whether a Probe message matches the specified host and sends a WS-Discovery ProbeMatches message with extended information if the match is made.
old-location: ncd\iwsdiscoverypublisher_matchprobeex_method.htm
tech.root: WsdApi
ms.assetid: d2441bdc-848b-48c4-bc4e-5b8f854cc4a5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisher interface,MatchProbeEx method, IWSDiscoveryPublisher.MatchProbeEx, IWSDiscoveryPublisher::MatchProbeEx, MatchProbeEx, MatchProbeEx method, MatchProbeEx method,IWSDiscoveryPublisher interface, ncd.iwsdiscoverypublisher_matchprobeex_method, wsddisco/IWSDiscoveryPublisher::MatchProbeEx
ms.topic: method
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryPublisher.MatchProbeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDiscoveryPublisher::MatchProbeEx


## -description


Determines whether a <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> message matches the specified host and sends a WS-Discovery <a href="https://msdn.microsoft.com/58d3d016-ae29-4090-9b88-e1125db59c95">ProbeMatches</a> message with extended information if the match is made.


## -parameters




### -param pProbeMessage [in]

Pointer to a <a href="https://msdn.microsoft.com/e5352a78-3ece-45d3-bf95-2d922065e3d5">WSD_SOAP_MESSAGE</a> structure that represents the Probe message passed to the notification sink's ProbeHandler.


### -param pMessageParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a> object that represents the transmission parameters passed in to the notification sink's ProbeHandler.


### -param pszId [in]

The logical or physical address of the device, which is used as the device endpoint address. A logical address is of the form <code>urn:uuid:{guid}</code>. A physical address can be a URI prefixed by http or https, or simply a URI prefixed by <code>uri</code>. Whenever possible, use a logical address.


### -param ullMetadataVersion [in]

Current metadata version.

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

If <i>pTypesList</i> is specified, <a href="https://msdn.microsoft.com/657f50ad-128f-4ccb-b89a-ed88f5d9b381">MatchProbe</a> will use WS-Discovery matching logic to verify that the types in the list match the types specified in <i>pProbeMessage</i>.


### -param pScopesList [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/86d77741-39c3-44bd-b072-d2d4eb99e488">WSD_URI_LIST</a> structure that represents the list of matching scopes supported by the publishing host. The list contains  hash values in string form. May be <b>NULL</b>.

If <i>pScopesList</i> is specified, <a href="https://msdn.microsoft.com/657f50ad-128f-4ccb-b89a-ed88f5d9b381">MatchProbe</a> will use WS-Discovery matching logic to verify that the scopes in the list match the scopes specified in <i>pProbeMessage</i>.


### -param pXAddrsList [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/86d77741-39c3-44bd-b072-d2d4eb99e488">WSD_URI_LIST</a> structure that represents the list of transport addresses supported by the publishing host. Each transport address string contains an address and port number which can be used for connection by a remote host. May be <b>NULL</b>.


### -param pHeaderAny [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that contains an XML element to be inserted in the "ANY" section of the header.


### -param pReferenceParameterAny [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that contains an XML element  to be inserted in the "ANY" section of the reference parameter properties.


### -param pPolicyAny [in, optional]

Not used.


### -param pEndpointReferenceAny [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that contains an XML element  to be inserted in the "ANY" section of the endpoint.


### -param pAny [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that contains an XML element  to be inserted in the "ANY" section of the message body.


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



<b>MatchProbeEx</b> should be called only when the discovery publisher has issued a <a href="https://msdn.microsoft.com/d92ce49c-308b-49e2-9646-f1eec2151441">ProbeHandler</a> callback. <i>pProbeMessage</i> and <i>pMessageParameters</i> are passed directly from the callback into <b>MatchProbeEx</b>. The <b>ProbeHandler</b> also passes information required by the publisher to determine if the supplied Probe message matches and, if so, to issue a ProbeMatches response if appropriate.

<b>MatchProbeEx</b> sends ProbeMatches messages on all bound adapters and automatically issues message retransmissions when required by WS-Discovery.

The parameters referring to <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structures can be used to extend the contents of the ProbeMatches message being sent with custom information.




## -see-also




<a href="https://msdn.microsoft.com/4fff1328-d315-4a26-b7d8-43a273133e08">IWSDiscoveryPublisher</a>
 

 

