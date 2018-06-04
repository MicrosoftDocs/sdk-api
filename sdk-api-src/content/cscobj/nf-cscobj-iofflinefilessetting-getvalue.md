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

# IOfflineFilesSetting::GetValue


## -description


Retrieves the value of a particular Offline Files setting.


## -parameters




### -param pvarValue [out]

Receives the value associated with the setting.  This value is determined based on system policy, preferences and system defaults.

The method initializes the <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> prior to storing the setting value in it.


### -param pbSetByPolicy [out]

Receives <b>TRUE</b> if the value was set by policy, <b>FALSE</b> if the value was determined by preference or default.


## -returns



<b>S_OK</b> if the value query is successful or an error value otherwise.




## -remarks



The value returned in the <i>pvarValue</i> parameter is determined as follows:

<ol>
<li>If machine policy exists, use it.</li>
<li>Otherwise, if user policy exists, use it.</li>
<li>Otherwise, if machine preference exists, use it.</li>
<li>Otherwise, if user preference exists, use it.</li>
<li>Otherwise, use the system default value.</li>
</ol>
The primary intent of the <i>pbSetByPolicy</i> parameter is to allow the caller to disable UI associated with a setting when the setting has been configured through Group Policy.

It is important to note that policy cannot be set through the Offline Files API.  Policy can be set only through the Group Policy mechanism.  The Offline Files API only supports querying policy values.




## -see-also




<a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a>
 

 

