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

# WscRegisterForChanges function


## -description


Registers a callback function to be run when Windows Security Center (WSC) detects a change that could affect the health of one of the security providers.


## -parameters




### -param Reserved [in]

Reserved.  Must be <b>NULL</b>.


### -param phCallbackRegistration [out]

A pointer to a handle to the callback registration. When you are finished using the callback function, unregister it by calling the <a href="https://msdn.microsoft.com/cfb0d076-bd8b-4483-a036-51c77b8181c9">WscUnRegisterChanges</a> function.


### -param lpCallbackAddress [in]

A pointer to the application-defined function to be called when a change to the WSC service occurs. This function is also called when the WSC service is started or stopped.


### -param pContext [in]

A pointer to a variable to be passed as  the <i>lpParameter</i> parameter to the function pointed to by the <i>lpCallbackAddress</i> parameter.


## -returns



Returns S_OK if the function succeeds, otherwise returns an error code.




## -remarks



When you want to cease receiving notification to your callback method, you can unregister it by calling the <a href="https://msdn.microsoft.com/cfb0d076-bd8b-4483-a036-51c77b8181c9">WscUnRegisterChanges</a> function.




## -see-also




<a href="https://msdn.microsoft.com/cfb0d076-bd8b-4483-a036-51c77b8181c9">WscUnRegisterChanges</a>
 

 

