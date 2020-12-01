---
UID: NF:wsdclient.IWSDServiceProxy.GetServiceMetadata
title: IWSDServiceProxy::GetServiceMetadata (wsdclient.h)
description: Retrieves the metadata for the IWSDServiceProxy object.
helpviewer_keywords: ["GetServiceMetadata","GetServiceMetadata method","GetServiceMetadata method","IWSDServiceProxy interface","IWSDServiceProxy interface","GetServiceMetadata method","IWSDServiceProxy.GetServiceMetadata","IWSDServiceProxy::GetServiceMetadata","ncd.iwsdserviceproxy_getservicemetadata_method","wsdclient/IWSDServiceProxy::GetServiceMetadata"]
old-location: ncd\iwsdserviceproxy_getservicemetadata_method.htm
tech.root: ncd
ms.assetid: 552da68f-6e6a-44b2-8c95-e29bc67de3c2
ms.date: 12/05/2018
ms.keywords: GetServiceMetadata, GetServiceMetadata method, GetServiceMetadata method,IWSDServiceProxy interface, IWSDServiceProxy interface,GetServiceMetadata method, IWSDServiceProxy.GetServiceMetadata, IWSDServiceProxy::GetServiceMetadata, ncd.iwsdserviceproxy_getservicemetadata_method, wsdclient/IWSDServiceProxy::GetServiceMetadata
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
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
 - IWSDServiceProxy::GetServiceMetadata
 - wsdclient/IWSDServiceProxy::GetServiceMetadata
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
 - IWSDServiceProxy.GetServiceMetadata
---

# IWSDServiceProxy::GetServiceMetadata


## -description

Retrieves the metadata for the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> object.

## -parameters

### -param ppServiceMetadata [out]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_service_metadata">WSD_SERVICE_METADATA</a> structure that specifies service metadata. Do not release this object.

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppServiceMetadata</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This metadata is also available as part of the metadata produced by <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-gethostmetadata">IWSDDeviceProxy::GetHostMetadata</a>.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a>