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

# IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs


## -description



        The <b>GetObjectIDsFromPersistentUniqueIDs</b> method retrieves the current object ID of one or more objects, given their persistent unique IDs (PUIDs).
      


## -parameters




### -param pPersistentUniqueIDs [in]


            Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a> interface that contains one or more persistent unique ID (PUID) string values (type VT_LPWSTR).
          


### -param ppObjectIDs [out]


            Pointer to an <b>IPortableDevicePropVariantCollection</b> interface pointer that contains the retrieved object IDs, as type <b>VT_LPWSTR</b>. The retrieved IDs will be in the same order as the submitted PUIDs; if a value could not be found, it is indicated by an empty string. The caller must release this interface when it is done with it.
          


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
At least one of the required arguments was a <b>NULL</b> pointer.

</td>
</tr>
</table>
 




## -remarks




        Windows Portable Devices Object IDs are unique across the device, but may be different across sessions. An Object ID can change when the application reconnects to the device.
      


        Certain applications, such as synchronization engines, require a way to identify the object across connection sessions. Every object has a WPD_OBJECT_PERSISTENT_UNIQUE_ID property, which indicates an identifier that is persistent across sessions. Applications can read and save this property in their initial session, by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a> method.
      


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/146f8943-d4e1-4b87-a812-e534082a4f14">Retrieving an Object Identifier from a Persistent Unique Identifier</a>


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a03c673-8e7f-41a4-81ba-88406af2762d">IPortableDeviceContent Interface</a>



<a href="https://msdn.microsoft.com/146f8943-d4e1-4b87-a812-e534082a4f14">Retrieving an Object Identifier from a Persistent Unique Identifier</a>
 

 

