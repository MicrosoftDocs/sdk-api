---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetEventOptions
title: IPortableDeviceCapabilities::GetEventOptions
author: windows-sdk-content
description: The GetEventOptions method retrieves all the supported options for the specified event on the device.
old-location: wpdsdk\iportabledevicecapabilities_geteventoptions.htm
old-project: wpd_sdk
ms.assetid: b4d3495b-b2d3-4d0d-8dc6-df030a52ab3f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetEventOptions, GetEventOptions method [Windows Portable Devices SDK], GetEventOptions method [Windows Portable Devices SDK],IPortableDeviceCapabilities method, IPortableDeviceCapabilities method [Windows Portable Devices SDK],GetEventOptions method, IPortableDeviceCapabilities.GetEventOptions, IPortableDeviceCapabilities::GetEventOptions, IPortableDeviceCapabilitiesGetEventOptions, portabledeviceapi/IPortableDeviceCapabilities::GetEventOptions, wpdsdk.iportabledevicecapabilities_geteventoptions
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
 - IPortableDeviceCapabilities.GetEventOptions
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceCapabilities::GetEventOptions


## -description


The <b>GetEventOptions</b> method retrieves all the supported options for the specified event on the device.
      


## -parameters




### -param Event [in]

A <b>REFGUID</b> that specifies a event to query for supported options. For a list of the events that are defined by Windows Portable Devices, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff543067">Events</a>.
          


### -param ppOptions [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that contains the supported options. If no options are supported, this will not contain any values. The caller must release this interface when it is done with it.
          


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



<a href="https://msdn.microsoft.com/en-us/library/Dd319362(v=VS.85).aspx">IPortableDeviceCapabilities Interface</a>
 

 

