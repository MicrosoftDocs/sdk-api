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

# IWTSProtocolConnection::GetUserData


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetUserData</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/fa05bcde-e4db-481b-88ab-57d070153517">IWRdsProtocolSettings::MergeSettings</a>.]

Sends merged policy settings to the protocol and requests user policy settings from the protocol.


## -parameters




### -param pPolicyData [in]

A pointer to a <a href="https://msdn.microsoft.com/407de671-f6e3-407e-9c97-11ea9ac8bdde">WTS_POLICY_DATA</a> structure that contains the merged Group Policy values.


### -param pClientData [in, out]

A pointer to a <a href="https://msdn.microsoft.com/be2f7338-44a8-433f-b45d-620b9b7e93c7">WTS_USER_DATA</a> structure that contains client property information.


## -remarks



The Remote Desktop Services service merges all policy data, including listener settings, client-provided data, and Group Policy data, before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

