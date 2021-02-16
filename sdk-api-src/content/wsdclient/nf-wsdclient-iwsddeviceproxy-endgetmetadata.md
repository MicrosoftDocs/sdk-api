---
UID: NF:wsdclient.IWSDDeviceProxy.EndGetMetadata
title: IWSDDeviceProxy::EndGetMetadata (wsdclient.h)
description: Ends an asynchronous request for metadata.
helpviewer_keywords: ["EndGetMetadata","EndGetMetadata method","EndGetMetadata method","IWSDDeviceProxy interface","IWSDDeviceProxy interface","EndGetMetadata method","IWSDDeviceProxy.EndGetMetadata","IWSDDeviceProxy::EndGetMetadata","ncd.iwsddeviceproxy_endgetmetadata","wsdclient/IWSDDeviceProxy::EndGetMetadata"]
old-location: ncd\iwsddeviceproxy_endgetmetadata.htm
tech.root: ncd
ms.assetid: c59ee37f-9189-4c32-8404-23cc94d76ad9
ms.date: 12/05/2018
ms.keywords: EndGetMetadata, EndGetMetadata method, EndGetMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,EndGetMetadata method, IWSDDeviceProxy.EndGetMetadata, IWSDDeviceProxy::EndGetMetadata, ncd.iwsddeviceproxy_endgetmetadata, wsdclient/IWSDDeviceProxy::EndGetMetadata
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
 - IWSDDeviceProxy::EndGetMetadata
 - wsdclient/IWSDDeviceProxy::EndGetMetadata
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
 - IWSDDeviceProxy.EndGetMetadata
---

# IWSDDeviceProxy::EndGetMetadata


## -description

Ends an asynchronous request for metadata and returns the metadata related to a device.

## -parameters

### -param pResult [in]

The <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> object returned by <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-begingetmetadata">BeginGetMetadata</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pResult</i> is <b>NULL</b>.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed. The metadata was not returned, was invalid, or a fault was generated.

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

EndGetMetadata must only be called after the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> object returned by <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-begingetmetadata">BeginGetMetadata</a> has indicated that the operation is complete.  Once EndGetMetadata has been called, the results of the latest metadata retrieval are accessible through the <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getallmetadata">GetAllMetadata</a>, <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-gethostmetadata">GetHostMetadata</a>, <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getthisdevicemetadata">GetThisDeviceMetadata</a>, and <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getthismodelmetadata">GetThisModelMetadata</a> methods.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a>