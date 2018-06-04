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

# WSManPluginOperationComplete function


## -description


Reports the completion of an operation by all operation entry points except for the <a href="https://msdn.microsoft.com/b3123f52-880b-4d14-a5a2-77c5924de99d">WSManPluginStartup</a> and <a href="https://msdn.microsoft.com/a9f72416-f6a7-4ba0-94d0-48f85393acab">WSManPluginShutdown</a> methods. 


## -parameters




### -param requestDetails [in]

A pointer to a <a href="https://msdn.microsoft.com/3191f2b3-e754-4f2d-ae8b-11da859c94b7">WSMAN_PLUGIN_REQUEST</a> structure that specifies the resource URI, options, locale, shutdown flag, and handle for the request.


### -param flags [in]

Reserved for future use. Must be zero.


### -param errorCode [in]

Reports any failure in the operation. If this parameter is not <b>NO_ERROR</b>, any result data that has not been sent will be discarded and the error will be sent.


### -param extendedInformation [in, optional]

Specifies an XML document that contains any extra error information that needs to be reported to the client. This parameter is ignored if <i>errorCode</i> is <b>NO_ERROR</b>. The user interface language of the thread should be used for localization.


## -returns



The method returns <b>NO_ERROR</b> if it succeeded; otherwise,  it returns an error code. If the operation is unsuccessful, the plug-in must stop the current operation and clean up any data associated with this operation. The <i>requestDetails</i> structure is not valid if an error is received and must not be passed to any other WinRM (WinRM) method.




## -remarks



The <b>WSManPluginOperationComplete</b> function is used to report the completion of the 
data stream for <a href="https://msdn.microsoft.com/59dff87b-17d5-4875-ad24-1520a04b05d2">WSManPluginReceive</a>.  The <a href="https://msdn.microsoft.com/3016612a-ce99-405b-afae-200bcad9ed20">WSManPluginShell</a> and <a href="https://msdn.microsoft.com/df4b4e7b-cf30-4eb0-b646-49b17c883a16">WSManPluginCommand</a> operations must also call this function when the shell and command operations are complete.



