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

# IWMDMStorage4::GetSpecifiedMetadata


## -description



The <b>GetSpecifiedMetadata</b> method retrieves one or more specific metadata properties from the storage.




## -parameters




### -param cProperties [in]

Count of properties to retrieve.


### -param ppwszPropNames [in]

Array of property names to retrieve. The length of this array should be equal to <i>cProperties</i>. The application should free this memory using <b>CoTaskMemFree</b>.


### -param ppMetadata [out]

Pointer to the returned <a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData</a> interface pointer, containing the retrieved values. The caller must release this interface when finished with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method gives the client control over which properties are retrieved. This can be more efficient than <a href="https://msdn.microsoft.com/7e436742-fb19-4e8e-98a2-d961c9f0ecbf">IWMDMStorage3::GetMetadata</a>, and is recommended when the client needs only a subset of properties supported by the storage.

If this method is used to retrieve data from a Windows Portable Devices (WPD) device, the data is returned in binary form in an <b>IPortableDeviceValues</b> object. The application should de-serialize this data in order to obtain the actual property values.

The method succeeds and returns WMDM_S_NOT_ALL_PROPERTIES_RETRIEVED even if some of the specified properties could not be retrieved (but at least one property was retrieved). The method fails and returns WMDM_E_NOTSUPPORTED if none of the specified properties could be retrieved.

Requesting a single property is a special case of this method. If the client requests a single property, the possible return codes are S_OK, E_INVALIDARG, and WMDM_E_NOTSUPPORTED. Thus, in the case of a single property, the method succeeds only if the property is successfully retrieved.




## -see-also




<a href="https://msdn.microsoft.com/9f803e1a-ff33-443a-9448-e8c875d77e51">Creating a Playlist on the Device</a>



<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>



<a href="https://msdn.microsoft.com/7e436742-fb19-4e8e-98a2-d961c9f0ecbf">IWMDMStorage3::GetMetadata</a>



<a href="https://msdn.microsoft.com/ac80cc08-0ff0-48ee-b9c6-e094f803b751">IWMDMStorage4 Interface</a>



<a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>
 

 

