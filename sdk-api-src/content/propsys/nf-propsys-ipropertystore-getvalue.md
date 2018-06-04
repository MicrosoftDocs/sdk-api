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

# IPropertyStore::GetValue


## -description


This method retrieves the data for a specific property.


## -parameters




### -param key




### -param pv

After the <code>IPropertyStore::GetValue</code> method returns successfully, this parameter points to a <a href="http://go.microsoft.com/fwlink/p/?linkid=106396">PROPVARIANT </a> structure that contains data about the property.


#### - Key

A reference to the PROPERTYKEY structure that is retrieved through <a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a>. The PROPERTYKEY structure also contains a globally unique identifier (GUID) for the property.


## -returns



Returns S_OK or INPLACE_S_TRUNCATED if successful, or an error value otherwise. 

INPLACE_S_TRUNCATED is returned to indicate that the returned PROPVARIANT was converted into a more canonical form. For example, this would be done to trim leading or trailing spaces from a string value. You must use the SUCCEEDED macro to check the return value, which treats INPLACE_S_TRUNCATED as a success code. The SUCCEEDED macro is defined in the Winerror.h file.




## -remarks



If the PROPERTYKEY referenced in key is not present in the property store, this method returns S_OK and the <a href="http://go.microsoft.com/fwlink/p/?linkid=106396">vt </a> member of the structure that is pointed to by pv is set to VT_EMPTY.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a>
 

 

