---
UID: NF:portabledeviceconnectapi.IPortableDeviceConnector.Disconnect
title: IPortableDeviceConnector::Disconnect (portabledeviceconnectapi.h)
description: Sends an asynchronous disconnect request to the MTP/Bluetooth device.
helpviewer_keywords: ["Disconnect","Disconnect method [Windows Portable Devices SDK]","Disconnect method [Windows Portable Devices SDK]","IPortableDeviceConnector interface","IPortableDeviceConnector interface [Windows Portable Devices SDK]","Disconnect method","IPortableDeviceConnector.Disconnect","IPortableDeviceConnector::Disconnect","devpkey/IPortableDeviceConnector::Disconnect","portabledeviceconnectapi/IPortableDeviceConnector::Disconnect","wpdsdk.iportabledeviceconnector_disconnect"]
old-location: wpdsdk\iportabledeviceconnector_disconnect.htm
tech.root: wpdsdk
ms.assetid: 0cc104e6-5e3a-4fce-ba3b-68f3fb94196b
ms.date: 12/05/2018
ms.keywords: Disconnect, Disconnect method [Windows Portable Devices SDK], Disconnect method [Windows Portable Devices SDK],IPortableDeviceConnector interface, IPortableDeviceConnector interface [Windows Portable Devices SDK],Disconnect method, IPortableDeviceConnector.Disconnect, IPortableDeviceConnector::Disconnect, devpkey/IPortableDeviceConnector::Disconnect, portabledeviceconnectapi/IPortableDeviceConnector::Disconnect, wpdsdk.iportabledeviceconnector_disconnect
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
 - IPortableDeviceConnector::Disconnect
 - portabledeviceconnectapi/IPortableDeviceConnector::Disconnect
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
 - IPortableDeviceConnector.Disconnect
---

# IPortableDeviceConnector::Disconnect


## -description

The <b>Disconnect</b> method sends an asynchronous disconnect request to the MTP/Bluetooth device.

## -parameters

### -param pCallback [in]

A pointer to an <a href="/windows/desktop/wpd_sdk/iconnectionrequestcallback">IConnectionRequestCallback</a> interface.

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
</table>

## -remarks

This method will queue a disconnect request and then return immediately.

To be notified when the request is complete, applications should provide a pointer to the <a href="/windows/desktop/wpd_sdk/iconnectionrequestcallback">IConnectionRequestCallback</a> interface. This will disconnect the MTP/Bluetooth link and remove the Windows Portable Devices (WPD) class driver stack for that device.

Once the disconnection completes, the WPD API will no longer enumerate this device.

## -see-also

<a href="/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector">IPortableDeviceConnector</a>