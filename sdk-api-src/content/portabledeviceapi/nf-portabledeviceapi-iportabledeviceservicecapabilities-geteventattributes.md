---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetEventAttributes
title: IPortableDeviceServiceCapabilities::GetEventAttributes (portabledeviceapi.h)
description: Retrieves the attributes of an event.helpviewer_keywords: ["GetEventAttributes","GetEventAttributes method [Windows Portable Devices SDK]","GetEventAttributes method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetEventAttributes method","IPortableDeviceServiceCapabilities.GetEventAttributes","IPortableDeviceServiceCapabilities::GetEventAttributes","portabledeviceapi/IPortableDeviceServiceCapabilities::GetEventAttributes","wpdsdk.iportabledeviceservicecapabilities_geteventattributes"]
old-location: wpdsdk\iportabledeviceservicecapabilities_geteventattributes.htm
tech.root: wpd_sdk
ms.assetid: cd3316aa-6d49-4d26-9ded-c9371ebea27b
ms.date: 12/05/2018
ms.keywords: GetEventAttributes, GetEventAttributes method [Windows Portable Devices SDK], GetEventAttributes method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetEventAttributes method, IPortableDeviceServiceCapabilities.GetEventAttributes, IPortableDeviceServiceCapabilities::GetEventAttributes, portabledeviceapi/IPortableDeviceServiceCapabilities::GetEventAttributes, wpdsdk.iportabledeviceservicecapabilities_geteventattributes
f1_keywords:
- portabledeviceapi/IPortableDeviceServiceCapabilities.GetEventAttributes
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceServiceCapabilities::GetEventAttributes


## -description


The <b>GetEventAttributes</b> method retrieves the attributes of an event.


## -parameters




### -param Event [in]

The event whose attributes are retrieved.


### -param ppAttributes [out]

The <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that receives the list of attributes.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



Possible attributes include the <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/wpd-attributes">WPD_EVENT_ATTRIBUTE_NAME</a>, WPD_EVENT_ATTRIBUTE_PARAMETERS, and WPD_EVENT_ATTRIBUTE_OPTIONS properties.
      


#### Examples

For an example of how to use this method, see <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/retrieving-supported-events">Retrieving Supported Service Events</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/retrieving-supported-events">Retrieving Supported Service Events</a>
 

 

