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

# IAutomaticUpdatesSettings3::put_NonAdministratorsElevated


## -description


<p class="CCE_Message">[<b>Set</b> is no longer supported. Also, starting with 
    Windows 10 calls to <b>Get</b> always return <b>VARIANT_TRUE</b>.]


Gets and sets a Boolean value that indicates whether non-administrators can perform some update-related actions without administrator approval.



This property is read/write.


## -parameters


## -remarks



The NonAdministratorsElevated property controls whether non-administrative users are allowed to perform some additional actions without elevation. It is equivalent to the “Allow all users to install updates on this computer” check box in the Windows Update settings dialog.




## -see-also




<a href="https://msdn.microsoft.com/2cc4d15f-eb8c-4db1-a81b-6eb3ee128121">IAutomaticUpdatesSettings3</a>
 

 

