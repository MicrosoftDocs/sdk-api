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

# IDataCollectorSet::SetCredentials


## -description


Specifies the user account under which the data collector set runs.  


## -parameters




### -param user [in]

A user account under which the data collector set runs. Specify the user name in the form <i>domain</i>\<i>user</i> or <i>user</i>@<i>domain</i>.


### -param password [in]

The password of the user account.


## -returns



The property returns S_OK if successful.




## -remarks



To clear the user credentials, set both parameters to <b>NULL</b>.

If you do not specify the credentials, PLA tries to run the set as LocalSystem if the current user is a member of the administrator group. 




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/32fe1dcf-9682-40fd-b301-45385fa33cbe">IDataCollectorSet::UserAccount</a>
 

 

