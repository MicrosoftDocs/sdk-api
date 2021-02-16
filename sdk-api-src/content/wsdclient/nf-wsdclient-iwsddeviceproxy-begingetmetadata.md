---
UID: NF:wsdclient.IWSDDeviceProxy.BeginGetMetadata
title: IWSDDeviceProxy::BeginGetMetadata (wsdclient.h)
description: Sends an asynchronous request for metadata.
helpviewer_keywords: ["BeginGetMetadata","BeginGetMetadata method","BeginGetMetadata method","IWSDDeviceProxy interface","IWSDDeviceProxy interface","BeginGetMetadata method","IWSDDeviceProxy.BeginGetMetadata","IWSDDeviceProxy::BeginGetMetadata","ncd.iwsddeviceproxy_begingetmetadata","wsdclient/IWSDDeviceProxy::BeginGetMetadata"]
old-location: ncd\iwsddeviceproxy_begingetmetadata.htm
tech.root: ncd
ms.assetid: 8aa71ef1-61b9-411b-9e8c-75470c638469
ms.date: 12/05/2018
ms.keywords: BeginGetMetadata, BeginGetMetadata method, BeginGetMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,BeginGetMetadata method, IWSDDeviceProxy.BeginGetMetadata, IWSDDeviceProxy::BeginGetMetadata, ncd.iwsddeviceproxy_begingetmetadata, wsdclient/IWSDDeviceProxy::BeginGetMetadata
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
 - IWSDDeviceProxy::BeginGetMetadata
 - wsdclient/IWSDDeviceProxy::BeginGetMetadata
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
 - IWSDDeviceProxy.BeginGetMetadata
---

# IWSDDeviceProxy::BeginGetMetadata


## -description

Sends an asynchronous request for metadata.

## -parameters

### -param ppResult [out]

Returns an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> object that can be used to determine whether an operation has completed.

## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
<i>ppResult</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The method could not be completed.

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

BeginGetMetadata will force the device proxy to send a metadata request to the host.  Once <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-endgetmetadata">EndGetMetadata</a> has been called, the results of the latest metadata retrieval are accessible through the <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getallmetadata">GetAllMetadata</a>, <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-gethostmetadata">GetHostMetadata</a>, <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getthisdevicemetadata">GetThisDeviceMetadata</a>, and <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getthismodelmetadata">GetThisModelMetadata</a> methods.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a>