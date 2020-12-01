---
UID: NF:wsdclient.IWSDDeviceProxy.GetThisDeviceMetadata
title: IWSDDeviceProxy::GetThisDeviceMetadata (wsdclient.h)
description: Retrieves device-specific metadata for this device.
helpviewer_keywords: ["GetThisDeviceMetadata","GetThisDeviceMetadata method","GetThisDeviceMetadata method","IWSDDeviceProxy interface","IWSDDeviceProxy interface","GetThisDeviceMetadata method","IWSDDeviceProxy.GetThisDeviceMetadata","IWSDDeviceProxy::GetThisDeviceMetadata","ncd.iwsddeviceproxy_getthisdevicemetadata_method","wsdclient/IWSDDeviceProxy::GetThisDeviceMetadata"]
old-location: ncd\iwsddeviceproxy_getthisdevicemetadata_method.htm
tech.root: ncd
ms.assetid: 95a87bb1-8e62-4ece-a7bc-2483ea282ede
ms.date: 12/05/2018
ms.keywords: GetThisDeviceMetadata, GetThisDeviceMetadata method, GetThisDeviceMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,GetThisDeviceMetadata method, IWSDDeviceProxy.GetThisDeviceMetadata, IWSDDeviceProxy::GetThisDeviceMetadata, ncd.iwsddeviceproxy_getthisdevicemetadata_method, wsdclient/IWSDDeviceProxy::GetThisDeviceMetadata
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
 - IWSDDeviceProxy::GetThisDeviceMetadata
 - wsdclient/IWSDDeviceProxy::GetThisDeviceMetadata
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
 - IWSDDeviceProxy.GetThisDeviceMetadata
---

# IWSDDeviceProxy::GetThisDeviceMetadata


## -description

Retrieves device-specific metadata for this device.

## -parameters

### -param ppThisDeviceMetadata [out]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_this_device_metadata">WSD_THIS_DEVICE_METADATA</a> structure that specifies the device-specific metadata of this device. 
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
<i>ppThisDeviceMetadata</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<b>GetThisDeviceMetadata</b> will not cause the device proxy to retrieve metadata from the device.  Instead, <b>GetThisDeviceMetadata</b> will return the metadata retrieved with the last call to <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-begingetmetadata">BeginGetMetadata</a> and <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-endgetmetadata">EndGetMetadata</a>.  If neither of these methods has been called, <b>GetThisDeviceMetadata</b> will return the metadata retrieved when the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> object was initialized.

Upon success, the memory at <i>ppMetadata</i> will be valid until <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-begingetmetadata">BeginGetMetadata</a> or <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-endgetmetadata">EndGetMetadata</a> is called or until the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> object is released.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a>