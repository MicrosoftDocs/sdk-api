---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetEventOptions
title: IPortableDeviceCapabilities::GetEventOptions
author: windows-sdk-content
description: The GetEventOptions method retrieves all the supported options for the specified event on the device.
old-location: wpdsdk\iportabledevicecapabilities_geteventoptions.htm
tech.root: wpd_sdk
ms.assetid: b4d3495b-b2d3-4d0d-8dc6-df030a52ab3f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetEventOptions, GetEventOptions method [Windows Portable Devices SDK], GetEventOptions method [Windows Portable Devices SDK],IPortableDeviceCapabilities method, IPortableDeviceCapabilities method [Windows Portable Devices SDK],GetEventOptions method, IPortableDeviceCapabilities.GetEventOptions, IPortableDeviceCapabilities::GetEventOptions, IPortableDeviceCapabilitiesGetEventOptions, portabledeviceapi/IPortableDeviceCapabilities::GetEventOptions, wpdsdk.iportabledevicecapabilities_geteventoptions
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceCapabilities.GetEventOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceCapabilities::GetEventOptions


## -description


The <b>GetEventOptions</b> method retrieves all the supported options for the specified event on the device.
      


## -parameters




### -param Event [in]

A <b>REFGUID</b> that specifies a event to query for supported options. For a list of the events that are defined by Windows Portable Devices, see <a href="https://msdn.microsoft.com/f579745a-5327-4c8b-bfa7-fe81d9657a3b">Events</a>.
          


### -param ppOptions [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface that contains the supported options. If no options are supported, this will not contain any values. The caller must release this interface when it is done with it.
          


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the arguments was a <b>NULL</b> pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b4d3495b-b2d3-4d0d-8dc6-df030a52ab3f">IPortableDeviceCapabilities</a>



<a href="wpdsdk.iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>
 

 

