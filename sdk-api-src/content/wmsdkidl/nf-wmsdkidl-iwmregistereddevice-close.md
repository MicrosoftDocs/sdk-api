---
UID: NF:wmsdkidl.IWMRegisteredDevice.Close
title: IWMRegisteredDevice::Close
author: windows-sdk-content
description: The Close method closes the device, if it is open. It also releases all resources associated with the device.
old-location: wmformat\iwmregistereddevice_close.htm
tech.root: wmformat
ms.assetid: 5d30eb82-1d5c-4d40-9dc9-7360e64cd55e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: Close, Close method [windows Media Format], Close method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],Close method, IWMRegisteredDevice.Close, IWMRegisteredDevice::Close, IWMRegisteredDeviceClose, wmformat.iwmregistereddevice_close, wmsdkidl/IWMRegisteredDevice::Close
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMRegisteredDevice.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMRegisteredDevice.Close
: 
---

# IWMRegisteredDevice::Close


## -description



The <b>Close</b> method closes the device, if it is open. It also releases all resources associated with the device.




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



Although this method returns immediately, it does not release resources associated with the device until after 30 to 60 seconds.




## -see-also




<a href="https://msdn.microsoft.com/6babdfbd-51d5-4973-9712-f79a95f5f367">IWMRegisteredDevice Interface</a>



<a href="https://msdn.microsoft.com/277f2724-5d82-4db7-96d9-af392b39fccf">IWMRegisteredDevice::Open</a>
 

 

