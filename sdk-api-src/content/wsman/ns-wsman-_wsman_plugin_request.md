---
UID: NS:wsman._WSMAN_PLUGIN_REQUEST
title: "_WSMAN_PLUGIN_REQUEST"
author: windows-sdk-content
description: Specifies information for a plug-in request.
old-location: winrm\wsman_plugin_request.htm
old-project: winrm
ms.assetid: 3191f2b3-e754-4f2d-ae8b-11da859c94b7
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: WSMAN_PLUGIN_REQUEST, WSMAN_PLUGIN_REQUEST structure [Windows Remote Management], _WSMAN_PLUGIN_REQUEST, winrm.wsman_plugin_request, wsman/WSMAN_PLUGIN_REQUEST
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSMAN_PLUGIN_REQUEST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_PLUGIN_REQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_PLUGIN_REQUEST structure


## -description


Specifies information for a plug-in request. A pointer to a <b>WSMAN_PLUGIN_REQUEST</b> structure is passed to all operation
entry points within the plug-in. All result notification methods use this
pointer to match the result with the request.  All information in the structure will stay valid until the plug-in calls <a href="https://msdn.microsoft.com/6cb47762-edfc-48d7-88ec-d62056ea1751">WSManPluginOperationComplete</a>
on the operation.


## -struct-fields




### -field senderDetails

A pointer to a <a href="https://msdn.microsoft.com/f68a9f75-6808-4dfa-b40f-061da88ead3c">WSMAN_SENDER_DETAILS</a> structure that specifies details about the client that initiated the request.


### -field locale

Specifies the locale that the user requested results to be in.  If the requested locale is not available, the following options are available:

<ul>
<li>The system locale is used.</li>
<li>The request is rejected with an invalid locale error.</li>
</ul>
Any call into the plug-in will have the locale on the thread set to the  locale that is specified in this member.  If the plug-in has other threads working on the request, the plug-in will need to set the locale accordingly on each thread that it uses.


### -field resourceUri

Specifies the <a href="windows_remote_management_glossary.htm">resource URI</a> for this operation.


### -field operationInfo

A pointer to a <a href="https://msdn.microsoft.com/a73029c6-d4e7-4cb3-ad0a-b71baffdbeb6">WSMAN_OPERATION_INFO</a> structure that contains extra information about the operation.  Some of the information in this structure will be <b>NULL</b> because not all of the parameters are relevant to all operations.


### -field shutdownNotification

If the operation is canceled, the <b>shutdownNotification</b> member is set to <b>TRUE</b>.


### -field shutdownNotificationHandle

If the operation is canceled, <b>shutdownNotification</b> is signaled.


### -field dataLocale

 




## -remarks



Operations must signal the callback for the operation to indicate it has been shut down. Operations are canceled in a hierarchical way to ensure that all follow-on operations are canceled before the top-level operations. A plug-in has two ways of handling the cancellation of an operation.   First, the plug-in can check the <b>shutdownNotification</b> Boolean value
if it iterates through a set of results.  Second, if the plug-in is more 
asynchronous in nature, the <b>shutdownNotificationHandle</b> can be used when queuing asynchronous notification threads.



