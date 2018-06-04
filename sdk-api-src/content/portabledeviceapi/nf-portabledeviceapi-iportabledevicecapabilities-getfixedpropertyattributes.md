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

# IPortableDeviceCapabilities::GetFixedPropertyAttributes


## -description



        The <b>GetFixedPropertyAttributes</b> method retrieves the standard property attributes for a specified property and format. Standard attributes are those that have the same value for all objects of the same format. For example, one device might not allow users to modify video file names; this device would return <b>WPD_PROPERTY_ATTRIBUTE_CAN_WRITE</b> with a value of False for WMV formatted objects. Attributes that can have different values for a format, or optional attributes, are not returned.
      


## -parameters




### -param Format [in]


            A <b>REFGUID</b> that specifies the format of the objects of interest. For format <b>GUID</b> values, see <a href="https://msdn.microsoft.com/b668f1c3-eed0-44c5-921f-e92c016130f0">Object Formats</a>.
          


### -param Key [in]


            A <b>REFPROPERTYKEY</b> that specifies the property that you want to know the attributes of. Properties defined by Windows Portable Devices are listed in <a href="https://msdn.microsoft.com/3bfbe8d0-6ad5-42de-afdd-d83328aaaa62">Properties and Attributes</a>.
          


### -param ppAttributes [out]


            Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that holds the attributes and their values. The caller must release this interface when it is done with it.
          


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
      


        Attributes describe properties. Example attributes are <b>WPD_PROPERTY_ATTRIBUTE_CAN_READ</b> and <b>WPD_PROPERTY_ATTRIBUTE_CAN_WRITE</b>. This method does not retrieve resource attributes.
      




## -see-also




<a href="https://msdn.microsoft.com/c292a509-f202-4136-bbf7-b4e82ef2b936">IPortableDeviceCapabilities Interface</a>



<a href="https://msdn.microsoft.com/bb2206ff-e1d4-4bc5-819b-b008a293c43d">IPortableDeviceProperties::GetPropertyAttributes</a>
 

 

