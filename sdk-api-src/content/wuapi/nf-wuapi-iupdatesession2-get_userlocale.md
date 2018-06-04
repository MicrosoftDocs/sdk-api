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

# IUpdateSession2::get_UserLocale


## -description


Gets and sets the preferred locale for which update information is retrieved.. 

If you do not specify the locale, the default is the user locale that   <a href="https://msdn.microsoft.com/0de3a2d8-e595-4068-805c-b9bcba7ada91">GetUserDefaultUILanguage</a> returns. If the information is not available in a specified locale or in the user locale, Windows Update Agent (WUA) tries to retrieve the information from the default update locale.

This property is read/write.


## -parameters


## -remarks



A search from an <b>UpdateSearch</b> object that was created from the <b>UpdateSession</b> object fails if the following conditions are true:

<ul>
<li>A user or a power user set the <b>UserLocale</b> property for the <a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a> interface to a locale.</li>
<li>The locale corresponds to a language that is not installed on the computer.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a>
 

 

