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

# SetUserGeoID function


## -description


<p class="CCE_Message">[<b>SetUserGeoID</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/0E5934DE-F526-45B4-9DAF-C8941F00C162">SetUserGeoName</a>.

]

Sets the geographical location identifier for the user. This identifier should have one of the values described in <a href="https://msdn.microsoft.com/6e424bd4-389c-4f51-9898-f60a8a818f89">Table of Geographical Locations</a>.


## -parameters




### -param GeoId [in]

Identifier for the geographical location of the user.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

<b>Windows XP, Windows Server 2003</b>: This function does not supply extended error information. Thus it is not appropriate for an application to call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> after this function. If the application does call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, it can return a value set by some previously called function.

If this function does not succeed, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_ACCESS_DISABLED_BY_POLICY. The group policy of the computer or the user has forbidden this operation.</li>
<li>ERROR_INTERNAL_ERROR. An unexpected error occurred in the function.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function writes to the registry the geographical location for a particular user instead of a particular application. This action affects the behavior of other applications run by the user. As a rule, the application should call this function only when the user has explicitly requested changes, but not for purely application-specific reasons.

<b>SetUserGeoID</b> is intended for use by applications that are designed to change user settings, such as the Windows Settings app. Other applications should not call this function.




## -see-also




<a href="https://msdn.microsoft.com/9d4d196d-4000-4866-a4c7-e7b9cb669c6f">GetUserGeoID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/0E5934DE-F526-45B4-9DAF-C8941F00C162">SetUserGeoName</a>



<a href="https://msdn.microsoft.com/6e424bd4-389c-4f51-9898-f60a8a818f89">Table of Geographical Locations</a>
 

 

