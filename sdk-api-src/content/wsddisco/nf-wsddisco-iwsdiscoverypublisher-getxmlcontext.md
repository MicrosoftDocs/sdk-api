---
UID: NF:wsddisco.IWSDiscoveryPublisher.GetXMLContext
title: IWSDiscoveryPublisher::GetXMLContext (wsddisco.h)
description: Gets the XML context associated with the device.
helpviewer_keywords: ["GetXMLContext","GetXMLContext method","GetXMLContext method","IWSDiscoveryPublisher interface","IWSDiscoveryPublisher interface","GetXMLContext method","IWSDiscoveryPublisher.GetXMLContext","IWSDiscoveryPublisher::GetXMLContext","ncd.iwsdiscoverypublisher_getxmlcontext","wsddisco/IWSDiscoveryPublisher::GetXMLContext"]
old-location: ncd\iwsdiscoverypublisher_getxmlcontext.htm
tech.root: ncd
ms.assetid: 9b849b17-0597-4e78-88c6-8ee95bcb754c
ms.date: 12/05/2018
ms.keywords: GetXMLContext, GetXMLContext method, GetXMLContext method,IWSDiscoveryPublisher interface, IWSDiscoveryPublisher interface,GetXMLContext method, IWSDiscoveryPublisher.GetXMLContext, IWSDiscoveryPublisher::GetXMLContext, ncd.iwsdiscoverypublisher_getxmlcontext, wsddisco/IWSDiscoveryPublisher::GetXMLContext
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
 - IWSDiscoveryPublisher::GetXMLContext
 - wsddisco/IWSDiscoveryPublisher::GetXMLContext
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
 - IWSDiscoveryPublisher.GetXMLContext
---

# IWSDiscoveryPublisher::GetXMLContext


## -description

Gets the  XML context associated with the device.

## -parameters

### -param ppContext [out]

Pointer to a pointer to an <a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a> object that represents the XML context.

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
<i>ppContext</i> is <b>NULL</b>.

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
</table>

## -remarks

Returns an optional context for the XML state of the transaction. If the service layer is used then this should be the context the XML namespaces and types were registered with.

## -see-also

<a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a>



<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a>