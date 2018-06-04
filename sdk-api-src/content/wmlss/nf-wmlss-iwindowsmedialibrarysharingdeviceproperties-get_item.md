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

# IWindowsMediaLibrarySharingDeviceProperties::get_Item


## -description


The <b>get_Item</b> method retrieves an <a href="https://msdn.microsoft.com/7b76cf66-0096-4b63-a30c-2df7d1a14527">IWindowsMediaLibrarySharingDeviceProperty</a> interface that represents an individual property for a media device.


## -parameters




### -param index [in]

The zero-based index of the property in the collection of all properties associated with the media device.


### -param property [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/7b76cf66-0096-4b63-a30c-2df7d1a14527">IWindowsMediaLibrarySharingDeviceProperty</a> interface.


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
 



