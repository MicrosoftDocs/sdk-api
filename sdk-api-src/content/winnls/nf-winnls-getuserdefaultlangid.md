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

# GetUserDefaultLangID function


## -description


Returns the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> of the Region Format setting for the current user.


## -parameters






## -returns



Returns the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> for the current user as set under <b>Control Panel</b> &gt; <b>Clock, Language, and Region</b> &gt; <b>Change date, time, or number formats</b> &gt; <b>Formats</b> tab &gt; <b>Format</b> dropdown.

For more information on language identifiers, see <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">Language Identifier Constants and Strings</a>.




## -remarks



The return value is not necessarily the same as that returned by <a href="https://msdn.microsoft.com/cf9d2f64-a8ad-46f8-9e91-a927b6b3ce08">GetSystemDefaultLangID</a>, even for a single-user computer.




## -see-also




<a href="https://msdn.microsoft.com/cf9d2f64-a8ad-46f8-9e91-a927b6b3ce08">GetSystemDefaultLangID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

