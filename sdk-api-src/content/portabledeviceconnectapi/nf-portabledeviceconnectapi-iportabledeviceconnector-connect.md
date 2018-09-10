---
UID: NF:portabledeviceconnectapi.IPortableDeviceConnector.Connect
title: IPortableDeviceConnector::Connect
author: windows-sdk-content
description: Sends an asynchronous connection request to the MTP/Bluetooth device.
old-location: wpdsdk\iportabledeviceconnector_connect.htm
tech.root: wpd_sdk
ms.assetid: 2bb5b124-3018-4619-bb8f-67fcfc8981d9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Connect, Connect method [Windows Portable Devices SDK], Connect method [Windows Portable Devices SDK],IPortableDeviceConnector interface, IPortableDeviceConnector interface [Windows Portable Devices SDK],Connect method, IPortableDeviceConnector.Connect, IPortableDeviceConnector::Connect, devpkey/IPortableDeviceConnector::Connect, portabledeviceconnectapi/IPortableDeviceConnector::Connect, wpdsdk.iportabledeviceconnector_connect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGuids.lib
 - PortableDeviceGuids.dll
api_name:
 - IPortableDeviceConnector.Connect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceConnector::Connect


## -description


The <b>Connect</b> method sends an asynchronous connection request to the MTP/Bluetooth device.


## -parameters




### -param pCallback [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/579f7a29-cd98-4d97-9f8e-9b786897df1c">IConnectionRequestCallback</a> interface if the application wishes to be notified when the request is complete; otherwise, <b>NULL</b>. If multiple requests are being sent simultaneously using the same <a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a> object, a different instance of the callback object must be used.


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



This method will queue a connect request and then return immediately. The connection request will result in a no-op if a device is already connected.

To be notified when the request is complete, applications should provide a pointer to the <a href="https://msdn.microsoft.com/579f7a29-cd98-4d97-9f8e-9b786897df1c">IConnectionRequestCallback</a> interface.

If a previously paired MTP/Bluetooth device is within range, applications can call this method to instantiate the Windows Portable Devices (WPD) class driver stack for that device, so that the device can be communicated to using the WPD API.




## -see-also




<a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a>
 

 

