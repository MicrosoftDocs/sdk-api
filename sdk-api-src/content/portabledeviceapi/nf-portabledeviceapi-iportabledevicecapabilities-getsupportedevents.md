---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetSupportedEvents
title: IPortableDeviceCapabilities::GetSupportedEvents
author: windows-sdk-content
description: The GetSupportedEvents method retrieves the supported events for this device.
old-location: wpdsdk\iportabledevicecapabilities_getsupportedevents.htm
old-project: wpd_sdk
ms.assetid: f5082b2b-d925-4f9d-bbfd-edcf4553a6fa
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: GetSupportedEvents, GetSupportedEvents method [Windows Portable Devices SDK], GetSupportedEvents method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetSupportedEvents method, IPortableDeviceCapabilities.GetSupportedEvents, IPortableDeviceCapabilities::GetSupportedEvents, IPortableDeviceCapabilitiesGetSupportedEvents, portabledeviceapi/IPortableDeviceCapabilities::GetSupportedEvents, wpdsdk.iportabledevicecapabilities_getsupportedevents
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDeviceCapabilities.GetSupportedEvents
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceCapabilities::GetSupportedEvents


## -description



        The <b>GetSupportedEvents</b> method retrieves the supported events for this device.
      


## -parameters




### -param ppEvents [out]


            Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a> interface that lists the supported events. The caller must release this interface when it is done with it.
          


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




<a href="https://msdn.microsoft.com/c292a509-f202-4136-bbf7-b4e82ef2b936">IPortableDeviceCapabilities Interface</a>
 

 

