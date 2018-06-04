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

# GetUserGeoID function


## -description


<p class="CCE_Message">[<b>GetUserGeoID</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/7938A5A1-E18E-4643-A07C-3354B4E94B5D">GetUserDefaultGeoName</a>.

]

Retrieves information about the geographical location of the user. For more information, see <a href="https://msdn.microsoft.com/6e424bd4-389c-4f51-9898-f60a8a818f89">Table of Geographical Locations</a>.


## -parameters




### -param GeoClass [in]

Geographical location class to return. Possible values are defined by the <a href="https://msdn.microsoft.com/27c2dec7-b5e7-47b7-8ce2-8dba3d0916bf">SYSGEOCLASS</a> enumeration.


## -returns



Returns the geographical location identifier of the user if <a href="https://msdn.microsoft.com/2e201a7e-6767-4908-b98c-f5b7f0544e60">SetUserGeoID</a> has been called before to set the identifier.

If no geographical location identifier has been set for the user, the function returns GEOID_NOT_AVAILABLE.




## -see-also




<a href="https://msdn.microsoft.com/7938A5A1-E18E-4643-A07C-3354B4E94B5D">GetUserDefaultGeoName</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/27c2dec7-b5e7-47b7-8ce2-8dba3d0916bf">SYSGEOCLASS</a>



<a href="https://msdn.microsoft.com/2e201a7e-6767-4908-b98c-f5b7f0544e60">SetUserGeoID</a>
 

 

