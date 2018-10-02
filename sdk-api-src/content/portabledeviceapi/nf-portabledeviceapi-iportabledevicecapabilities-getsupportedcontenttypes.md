---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetSupportedContentTypes
title: IPortableDeviceCapabilities::GetSupportedContentTypes
author: windows-sdk-content
description: The GetSupportedContentTypes method retrieves all supported content types for a specified functional object type on a device.
old-location: wpdsdk\iportabledevicecapabilities_getsupportedcontenttypes.htm
tech.root: wpd_sdk
ms.assetid: 5f56ca91-552f-4a52-8a68-225601c5f6f4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSupportedContentTypes, GetSupportedContentTypes method [Windows Portable Devices SDK], GetSupportedContentTypes method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetSupportedContentTypes method, IPortableDeviceCapabilities.GetSupportedContentTypes, IPortableDeviceCapabilities::GetSupportedContentTypes, IPortableDeviceCapabilitiesGetSupportedContentTypes, portabledeviceapi/IPortableDeviceCapabilities::GetSupportedContentTypes, wpdsdk.iportabledevicecapabilities_getsupportedcontenttypes
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
 - IPortableDeviceCapabilities.GetSupportedContentTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceCapabilities::GetSupportedContentTypes


## -description


The <b>GetSupportedContentTypes</b> method retrieves all supported content types for a specified functional object type on a device.
      


## -parameters




### -param Category [in]

A <b>REFGUID</b> that specifies a functional object category. To get a list of functional categories on the device, call <a href="https://msdn.microsoft.com/c444f9d6-7bef-4e0a-bcd8-6a6110986208">IPortableDeviceCapabilities::GetFunctionalCategories</a>.
          


### -param ppContentTypes [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/41224958-a5a0-4e09-8733-d0ae036f68b9">IPortableDevicePropVariantCollection</a> interface that lists all the supported object types for the specified functional object category. These object types will be <b>GUID</b> values of type VT_CLSID in the retrieved <b>PROPVARIANT</b> items. See <a href="https://msdn.microsoft.com/4c3da994-fe12-4cb8-8f11-c4930cae96af">Requirements for Objects</a> for a list of object types defined by Windows Portable Devices. The caller must release this interface when it is done with it.
          


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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd319362(v=VS.85).aspx">IPortableDeviceCapabilities Interface</a>



<a href="https://msdn.microsoft.com/1cedb8d9-2476-420c-bab4-c8a032af781b">Retrieving the Content Types Supported by a Device</a>
 

 

