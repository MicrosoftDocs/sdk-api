---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPortableDeviceCapabilities::GetSupportedFormatProperties


## -description



        The <b>GetSupportedFormatProperties</b> method retrieves the properties supported by objects of a specified format on the device.
      


## -parameters




### -param Format [in]


            A <b>REFGUID</b> that specifies the format of the object. For a list of formats that are defined by Windows Portable Devices, see <a href="https://msdn.microsoft.com/b668f1c3-eed0-44c5-921f-e92c016130f0">Object Formats</a>.
          


### -param ppKeys [out]


            Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597583">IPortableDeviceKeyCollection</a> interface that contains the supported properties for the specified format. For a list of properties defined by Windows Portable Devices, see <a href="https://msdn.microsoft.com/3bfbe8d0-6ad5-42de-afdd-d83328aaaa62">Properties and Attributes</a>. The caller must release this interface when it is done with it.
          


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




        You can specify <b>WPD_OBJECT_FORMAT_ALL</b> for the <i>Format</i> parameter to retrieve the complete set of property attributes.
      


        If an object does not have a value assigned to a specific property, or if the property was deleted, a device might not report the property at all when enumerating its properties. Another device might report the property, but with an empty string or a value of zero. In order to avoid this inconsistency, you can call this method to learn all the properties you can set on a specific object.
      




## -see-also




<a href="https://msdn.microsoft.com/c292a509-f202-4136-bbf7-b4e82ef2b936">IPortableDeviceCapabilities Interface</a>



<a href="https://msdn.microsoft.com/7568f5cf-2f9e-459c-ae08-d23b9e37ce4e">IPortableDeviceCapabilities::GetSupportedFormats</a>
 

 

