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

# AuthzSetAppContainerInformation function


## -description


The <b>AuthzSetAppContainerInformation</b> function sets the  app container and capability information in a current Authz context. If the passed in context already has an app container <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) set or if the passed in context is not a valid app container SID, this function fails.


## -parameters




### -param hAuthzClientContext [in]

	The handle to the client context to which the given app container SID and capability SIDs will be added.


### -param pAppContainerSid [in]

The app container SID.


### -param CapabilityCount [in]

The number of capability SIDs to be added. This value can be zero if no capability is to be added.


### -param pCapabilitySids [in, optional]

The capability SIDs to be added to the context. This value must be <b>NULL</b> when the <i>CapabilityCount</i> parameter is zero.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



