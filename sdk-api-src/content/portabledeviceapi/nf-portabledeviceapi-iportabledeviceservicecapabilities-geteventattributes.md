---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetEventAttributes
title: IPortableDeviceServiceCapabilities::GetEventAttributes
author: windows-sdk-content
description: Retrieves the attributes of an event.
old-location: wpdsdk\iportabledeviceservicecapabilities_geteventattributes.htm
tech.root: wpd_sdk
ms.assetid: cd3316aa-6d49-4d26-9ded-c9371ebea27b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetEventAttributes, GetEventAttributes method [Windows Portable Devices SDK], GetEventAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetEventAttributes method, IPortableDeviceServiceCapabilities.GetEventAttributes, IPortableDeviceServiceCapabilities::GetEventAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetEventAttributes, wpdsdk.iportabledeviceservicecapabilities_geteventattributes
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPortableDeviceServiceCapabilities.GetEventAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceServiceCapabilities::GetEventAttributes


## -description


The <b>GetEventAttributes</b> method retrieves the attributes of an event.


## -parameters




### -param Event [in]

The event whose attributes are retrieved.


### -param ppAttributes [out]

The <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface that receives the list of attributes.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



Possible attributes include the <a href="wpd_attributes.htm">WPD_EVENT_ATTRIBUTE_NAME</a>, WPD_EVENT_ATTRIBUTE_PARAMETERS, and WPD_EVENT_ATTRIBUTE_OPTIONS properties.
      


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>



<a href="https://msdn.microsoft.com/1bf3aa08-7ffc-417f-a67e-9eee042337b9">Retrieving Supported Service Events</a>
 

 

