---
UID: NF:wsdclient.IWSDDeviceProxy.GetHostMetadata
title: IWSDDeviceProxy::GetHostMetadata (wsdclient.h)
description: Retrieves class-specific metadata for the device describing the features of the device and the services it hosts.
helpviewer_keywords: ["GetHostMetadata","GetHostMetadata method","GetHostMetadata method","IWSDDeviceProxy interface","IWSDDeviceProxy interface","GetHostMetadata method","IWSDDeviceProxy.GetHostMetadata","IWSDDeviceProxy::GetHostMetadata","ncd.iwsddeviceproxy_gethostmetadata","wsdclient/IWSDDeviceProxy::GetHostMetadata"]
old-location: ncd\iwsddeviceproxy_gethostmetadata.htm
tech.root: ncd
ms.assetid: e1e81f75-baeb-4406-8de0-f575db573fe8
ms.date: 12/05/2018
ms.keywords: GetHostMetadata, GetHostMetadata method, GetHostMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,GetHostMetadata method, IWSDDeviceProxy.GetHostMetadata, IWSDDeviceProxy::GetHostMetadata, ncd.iwsddeviceproxy_gethostmetadata, wsdclient/IWSDDeviceProxy::GetHostMetadata
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
 - IWSDDeviceProxy::GetHostMetadata
 - wsdclient/IWSDDeviceProxy::GetHostMetadata
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
 - IWSDDeviceProxy.GetHostMetadata
---

# IWSDDeviceProxy::GetHostMetadata


## -description

Retrieves class-specific metadata for the device describing the features of the device and the services it hosts.

## -parameters

### -param ppHostMetadata [out]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_host_metadata">WSD_HOST_METADATA</a> structure that specifies metadata. 
Do not release this object.

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
<i>ppHostMetadata</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<b>GetHostMetadata</b> will not cause the device proxy to retrieve metadata from the device.  Instead, <b>GetHostMetadata</b> will return the metadata retrieved with the last call to <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-begingetmetadata">BeginGetMetadata</a> and <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-endgetmetadata">EndGetMetadata</a>.  If neither of these methods has been called, <b>GetHostMetadata</b> will return the metadata retrieved when the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> object was initialized.

Upon success, the memory at <i>ppMetadata</i> will be valid until <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-begingetmetadata">BeginGetMetadata</a> or <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-endgetmetadata">EndGetMetadata</a> is called or until the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> object is released.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a>