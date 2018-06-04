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

# IWTSProtocolConnection::IsUserAllowedToLogon


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::IsUserAllowedToLogon</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/4e2c5d2b-ec45-45ea-8bd3-71aaa0b15529">IWRdsProtocolConnection::IsUserAllowedToLogon</a>.]

Determines whether a user is allowed to log on to a session.


## -parameters




### -param SessionId [in]

An integer that contains the session ID associated with the user.


### -param UserToken [in]

A pointer to the user token handle.


### -param pDomainName [in]

A pointer to a string that contains the domain name for the user.


### -param pUserName [in]

A pointer to a string that contains the user name.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

