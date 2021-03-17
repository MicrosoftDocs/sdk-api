---
UID: NF:portabledeviceconnectapi.IPortableDeviceConnector.Cancel
title: IPortableDeviceConnector::Cancel (portabledeviceconnectapi.h)
description: Cancels a pending request to connect or disconnect an MTP/Bluetooth device.
helpviewer_keywords: ["Cancel","Cancel method [Windows Portable Devices SDK]","Cancel method [Windows Portable Devices SDK]","IPortableDeviceConnector interface","IPortableDeviceConnector interface [Windows Portable Devices SDK]","Cancel method","IPortableDeviceConnector.Cancel","IPortableDeviceConnector::Cancel","devpkey/IPortableDeviceConnector::Cancel","portabledeviceconnectapi/IPortableDeviceConnector::Cancel","wpdsdk.iportabledeviceconnector_cancel"]
old-location: wpdsdk\iportabledeviceconnector_cancel.htm
tech.root: wpdsdk
ms.assetid: 4cc3ecd1-f2b0-4e8e-8654-6445782153f3
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDeviceConnector interface, IPortableDeviceConnector interface [Windows Portable Devices SDK],Cancel method, IPortableDeviceConnector.Cancel, IPortableDeviceConnector::Cancel, devpkey/IPortableDeviceConnector::Cancel, portabledeviceconnectapi/IPortableDeviceConnector::Cancel, wpdsdk.iportabledeviceconnector_cancel
req.header: portabledeviceconnectapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceconnectapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceConnector::Cancel
 - portabledeviceconnectapi/IPortableDeviceConnector::Cancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGuids.lib
 - PortableDeviceGuids.dll
api_name:
 - IPortableDeviceConnector.Cancel
---

# IPortableDeviceConnector::Cancel


## -description

The <b>Cancel</b> method cancels a pending request to connect or disconnect an MTP/Bluetooth device. The callback object is used to identify the request. This method returns immediately, and the request will be cancelled asynchronously.

## -parameters

### -param pCallback [in]

A pointer to an <a href="/windows/desktop/wpd_sdk/iconnectionrequestcallback">IConnectionRequestCallback</a> interface. This value cannot be <b>NULL</b>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Either the <i>pCallback</i> parameter does not correspond to a pending connect or disconnect request, or this method has been already been called.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector">IPortableDeviceConnector</a>