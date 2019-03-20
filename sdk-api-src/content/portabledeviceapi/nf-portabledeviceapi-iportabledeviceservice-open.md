---
UID: NF:portabledeviceapi.IPortableDeviceService.Open
title: IPortableDeviceService::Open (portabledeviceapi.h)
author: windows-sdk-content
description: Opens a connection to the service.
old-location: wpdsdk\iportabledeviceservice_open.htm
tech.root: wpd_sdk
ms.assetid: 540d4320-42d4-48f0-8445-c74ff0dc1e1a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPortableDeviceService interface [Windows Portable Devices SDK],Open method, IPortableDeviceService.Open, IPortableDeviceService::Open, Open, Open method [Windows Portable Devices SDK], Open method [Windows Portable Devices SDK],IPortableDeviceService interface, portabledeviceapi/IPortableDeviceService::Open, wpdsdk.iportabledeviceservice_open
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceService.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceService::Open


## -description


The <b>Open</b> method opens a connection to the service.


## -parameters




### -param pszPnPServiceID [in]

The Plug and Play (PnP) identifier for the service, which is the same identifier that is retrieved by the <a href="https://msdn.microsoft.com/c73261a5-1436-4706-8d8b-ff8183429ac4">GetPnPServiceId</a> method.


### -param pClientInfo [in]

The <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface specifying the client information.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The PnP identifier specified by the <i>pszPnPServiceID</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> parameter was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_WPD_SERVICE_ALREADY_OPENED</b></dt>
</dl>
</td>
<td width="60%">
This method has already been called for the service.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService Interface</a>



<a href="https://msdn.microsoft.com/722d657d-332a-40df-ac30-bc2050deda74">Opening a Service</a>
 

 

