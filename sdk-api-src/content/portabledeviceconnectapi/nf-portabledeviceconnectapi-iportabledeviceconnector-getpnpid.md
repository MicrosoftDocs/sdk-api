---
UID: NF:portabledeviceconnectapi.IPortableDeviceConnector.GetPnPID
title: IPortableDeviceConnector::GetPnPID
author: windows-sdk-content
description: Retrieves the connector's Plug and Play (PnP) device identifier.
old-location: wpdsdk\iportabledeviceconnector_getpnpid.htm
old-project: wpd_sdk
ms.assetid: 39e7702a-f23e-4f04-8524-06a0fcc025a1
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: GetPnPID, GetPnPID method [Windows Portable Devices SDK], GetPnPID method [Windows Portable Devices SDK],IPortableDeviceConnector interface, IPortableDeviceConnector interface [Windows Portable Devices SDK],GetPnPID method, IPortableDeviceConnector.GetPnPID, IPortableDeviceConnector::GetPnPID, devpkey/IPortableDeviceConnector::GetPnPID, portabledeviceconnectapi/IPortableDeviceConnector::GetPnPID, wpdsdk.iportabledeviceconnector_getpnpid
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGuids.lib
 - PortableDeviceGuids.dll
api_name:
 - IPortableDeviceConnector.GetPnPID
product: Windows
targetos: Windows
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceConnector::GetPnPID


## -description


The <b>GetPnPID</b> method retrieves the connector's Plug and Play (PnP) device identifier.


## -parameters




### -param ppwszPnPID [out]

The PnP device identifier.


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



The identifier retrieved by this method corresponds to a handle to the MTP/Bluetooth Bus Enumerator device node that receives connect and disconnect IOCTL requests for a paired MTP/Bluetooth device.  Applications can use this identifier with the SetupAPI functions to access the device node.

Once the application no longer needs the identifier specified by the <i>ppwszPnPID</i> parameter, it must call the <b>CoTaskMemAlloc</b> function to free the identifier.




## -see-also




<a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a>
 

 

