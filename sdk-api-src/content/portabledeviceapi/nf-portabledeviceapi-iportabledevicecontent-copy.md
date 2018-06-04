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

# IPortableDeviceContent::Copy


## -description



        The <b>Copy</b> method copies objects from one location on a device to another.
      


## -parameters




### -param pObjectIDs


            A collection of object identifiers for the objects that this method will copy.
          


### -param pszDestinationFolderObjectID


            An object identifier for the destination folder (or functional storage) into which this method will copy the specified objects.
          


### -param ppResults [out]


            A collection of VT_ERROR values indicating the success or failure of copying a particular element. The first error value corresponds to the first object in the collection of object identifiers, the second to the second element, and so on. This argument can be <b>NULL</b>.
          


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The copy operation failed for at least one object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The application does not have the rights to copy one of the specified objects.

</td>
</tr>
</table>
 




## -remarks




        If the specified device supports copy operations to a functional storage, the <i>pszDestinationFolderObjectID</i> parameter may specify the identifier for a functional storage.
      




## -see-also




<a href="https://msdn.microsoft.com/7a03c673-8e7f-41a4-81ba-88406af2762d">IPortableDeviceContent Interface</a>
 

 

