---
UID: NF:wsddisco.IWSDiscoveryPublisher.PublishEx
title: IWSDiscoveryPublisher::PublishEx (wsddisco.h)
description: Announces the presence of a network host by sending a Hello message with extended information.
helpviewer_keywords: ["IWSDiscoveryPublisher interface","PublishEx method","IWSDiscoveryPublisher.PublishEx","IWSDiscoveryPublisher::PublishEx","PublishEx","PublishEx method","PublishEx method","IWSDiscoveryPublisher interface","ncd.iwsdiscoverypublisher_publishex_method","wsddisco/IWSDiscoveryPublisher::PublishEx"]
old-location: ncd\iwsdiscoverypublisher_publishex_method.htm
tech.root: ncd
ms.assetid: f4a1f93d-071b-4244-b4e4-ed7e7bb7432b
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisher interface,PublishEx method, IWSDiscoveryPublisher.PublishEx, IWSDiscoveryPublisher::PublishEx, PublishEx, PublishEx method, PublishEx method,IWSDiscoveryPublisher interface, ncd.iwsdiscoverypublisher_publishex_method, wsddisco/IWSDiscoveryPublisher::PublishEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDiscoveryPublisher::PublishEx
 - wsddisco/IWSDiscoveryPublisher::PublishEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryPublisher.PublishEx
---

# IWSDiscoveryPublisher::PublishEx


## -description

Announces the presence of a network host by sending a <a href="/windows/desktop/WsdApi/hello-message">Hello</a> message with extended information.

## -parameters

### -param pszId [in]

The logical or physical address of the device, which is used as the device endpoint address. A logical address is of the form <code>urn:uuid:{guid}</code>. A physical address can be a URI prefixed by http or https, or simply a URI prefixed by <code>uri</code>. Whenever possible, use a logical address.

### -param ullMetadataVersion [in]

Current metadata version.

<div class="alert"><b>Note</b>  For compatibility with the WS-Discovery specification, this value must be less than or equal to UINT_MAX (4294967295).</div>
<div> </div>

### -param ullInstanceId [in]

Identifier for the current instance of the device being published. This identifier must be incremented whenever the service is restarted. For more information about instance identifiers, see Appendix I of the <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery specification</a>.

<div class="alert"><b>Note</b>  For compatibility with the WS-Discovery specification, this value must be less than or equal to UINT_MAX (4294967295).</div>
<div> </div>

### -param ullMessageNumber [in]

Counter within the scope of the instance identifier for the current message. The message number must be incremented for each message.

<div class="alert"><b>Note</b>  For compatibility with the WS-Discovery specification, this value must be less than or equal to UINT_MAX (4294967295).</div>
<div> </div>

### -param pszSessionId [in, optional]

Unique identifier within the scope of the instance identifier for the current session. This parameter corresponds to the sequence identifier in the AppSequence block in the Probe message. For more information about sequence identifiers, see Appendix I of the <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery specification</a>.

This parameter may be <b>NULL</b>.

### -param pTypesList [in, optional]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_name_list">WSD_NAME_LIST</a> structure that represents the list of types supported by the publishing host. May be <b>NULL</b>.

### -param pScopesList [in, optional]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_uri_list">WSD_URI_LIST</a> structure that represents the list of matching scopes supported by the publishing host. The list contains hash values in string form. May be <b>NULL</b>.

### -param pXAddrsList [in, optional]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_uri_list">WSD_URI_LIST</a> structure that represents the list of transport addresses supported by the publishing host. Each transport address string contains an address and port number which can be used for connection by a remote host. May be <b>NULL</b>.

### -param pHeaderAny [in, optional]

Pointer to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that contains an XML element to be inserted in the "ANY" section of the header.

### -param pReferenceParameterAny [in, optional]

Pointer to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that contains an XML element to be inserted in the "ANY" section of the reference parameter properties.

### -param pPolicyAny [in, optional]

Not used.

### -param pEndpointReferenceAny [in, optional]

Pointer to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that contains an XML element  to be inserted in the "ANY" section of the endpoint.

### -param pAny [in, optional]

Pointer to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that contains an XML element  to be inserted in the "ANY" section of the message body.

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
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_CALLBACK_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
There is no registered notification sink. To attach a sink, call <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-registernotificationsink">RegisterNotificationSink</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The publisher has not been started. Attaching a notification sink starts the publisher. To attach a sink, call <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-registernotificationsink">RegisterNotificationSink</a>.

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

If successful, <b>PublishEx</b> will send a WS-Discovery Hello message to the local subnet with the provided information. 

The parameters referring to <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structures can be used to extend the contents of the Hello message being sent with custom information.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a>