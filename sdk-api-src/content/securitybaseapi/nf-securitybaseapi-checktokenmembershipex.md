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

# CheckTokenMembershipEx function


## -description


The <b>CheckTokenMembershipEx</b> function determines whether the specified SID is enabled in the specified token.


## -parameters




### -param TokenHandle [in, optional]

A handle to an access token. If present, this token is checked for the SID. If not present, then the current effective token is used. This must be an impersonation token.


### -param SidToCheck [in]

A pointer to a SID structure. The function checks for the presence of this SID in the presence of the token.


### -param Flags [in]

Flags that affect the behavior of the function. Currently the only valid flag is CTMF_INCLUDE_APPCONTAINER which allows app containers to pass the call as long as the other requirements of the token are met, such as the group specified is present and enabled.


### -param IsMember [out]

<b>TRUE</b> if the SID is enabled in the token; otherwise, <b>FALSE</b>.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



