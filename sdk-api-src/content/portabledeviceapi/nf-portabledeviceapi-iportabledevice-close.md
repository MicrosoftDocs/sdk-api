---
UID: NF:portabledeviceapi.IPortableDevice.Close
title: IPortableDevice::Close
author: windows-sdk-content
description: The Close method closes the connection with the device.
old-location: wpdsdk\iportabledevice_close.htm
old-project: wpd_sdk
ms.assetid: aa60a439-7589-465e-98e5-56b93d594f96
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: Close, Close method [Windows Portable Devices SDK], Close method [Windows Portable Devices SDK],IPortableDevice interface, IPortableDevice interface [Windows Portable Devices SDK],Close method, IPortableDevice.Close, IPortableDevice::Close, IPortableDeviceClose, portabledeviceapi/IPortableDevice::Close, wpdsdk.iportabledevice_close
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDevice.Close
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDevice::Close


## -description



        The <b>Close</b> method closes the connection with the device.
      


## -parameters






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




        You should not usually need to call this method yourself. When the last reference to the <a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice</a> interface  is released, Windows Portable Devices calls <b>Close</b> for you. Calling this method manually forces the connection to the device to close, and any Windows Portable Devices objects hosted on this device will cease to function. You can call <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> to reopen the connection.
      




## -see-also




<a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice Interface</a>



<a href="https://msdn.microsoft.com/d505fc34-9b6d-417a-a53e-e74773dcc8a4">IPortableDevice::Open</a>
 

 

