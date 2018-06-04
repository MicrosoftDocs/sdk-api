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

# SspiIsPromptingNeeded function


## -description


Indicates whether an error returned after a call to either the <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext</a> or the <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext</a> function requires an additional call to the <a href="https://msdn.microsoft.com/2af2ac00-0e91-4384-9ffa-3e100df218c1">SspiPromptForCredentials</a> function.


## -parameters




### -param ErrorOrNtStatus [in]

The error to test.


## -returns



<b>TRUE</b> if the error specified by the <i>ErrorOrNtStatus</i> parameter indicates that an additional call to <a href="https://msdn.microsoft.com/2af2ac00-0e91-4384-9ffa-3e100df218c1">SspiPromptForCredentials</a> is necessary; otherwise, <b>FALSE</b>.



