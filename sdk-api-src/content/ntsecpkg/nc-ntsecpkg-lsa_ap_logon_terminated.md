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

# LSA_AP_LOGON_TERMINATED callback function


## -description


Used to notify an authentication package when a logon session terminates.
			A logon session terminates when the last token referencing the logon session is deleted.


## -parameters




### -param LogonId [in]

Pointer to the logon ID of the session that just ended.


## -returns



This function does not return a value.




## -remarks



When <b>LsaApLogonTerminated</b> is called, an authentication package should release any resources held for the logon ID, such as credentials created within the LSA. The LSA does not automatically perform this cleanup.



