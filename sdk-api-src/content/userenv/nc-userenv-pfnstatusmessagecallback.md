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

# PFNSTATUSMESSAGECALLBACK callback function


## -description


The
    <b>StatusMessageCallback</b> function is an application-defined callback function used to display status messages when applying policy. The <b>PFNSTATUSMESSAGECALLBACK</b> type defines a pointer to this callback function. 
<b>StatusMessageCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param bVerbose [in]

Specifies whether the message is verbose. If this parameter is <b>TRUE</b>, the message is verbose. If this parameter is <b>FALSE</b>, the message is not verbose.


### -param lpMessage [in]

Pointer to a buffer that contains the message string.


## -returns



If the message was displayed successfully, return <b>ERROR_SUCCESS</b>. Otherwise, return a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



Pass a pointer to the 
<b>StatusMessageCallback</b> function when the system calls the 
<a href="https://msdn.microsoft.com/f639c11c-ee65-45b6-ba0d-f39c825b3d80">ProcessGroupPolicy</a> or the 
<a href="https://msdn.microsoft.com/df77fece-6e81-4a85-847a-fef3ba775e93">ProcessGroupPolicyEx</a> callback function.

The status user interface has two modes: standard and verbose. Verbose messages are displayed only when the computer is in verbose mode. To enable verbose mode, set the following registry value to 1, log out, and log on. There is no need to restart the computer.


<b>HKEY_LOCAL_MACHINE</b>\<b>Software</b>\<b>Microsoft</b>\<b>Windows NT</b>\<b>CurrentVersion</b>\<b>Winlogon</b>\<b>VerboseStatus</b>



<div class="alert"><b>Warning</b>  Do not call the 
<b>StatusMessageCallback</b> function from a background thread because you may overwrite another thread's status message.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/f639c11c-ee65-45b6-ba0d-f39c825b3d80">ProcessGroupPolicy</a>



<a href="https://msdn.microsoft.com/df77fece-6e81-4a85-847a-fef3ba775e93">ProcessGroupPolicyEx</a>
 

 

