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

# IWTSSBPlugin::WTSSBX_SessionChangeNotification


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a> interface.]

Notifies the plug-in that a change, such as a logon, logoff, disconnect, or reconnect, occurred in the session.


## -parameters




### -param NotificationType [in]

A <a href="https://msdn.microsoft.com/06da6e20-a4de-4e2d-8f42-6d99b738226c">WTSSBX_NOTIFICATION_TYPE</a> type that specifies the type of change that occurred.


### -param MachineId [in]

The ID of the server on which the session change occurred.


### -param NumOfSessions [in]

The number of elements in the <i>SessionInfo</i> array.


### -param SessionInfo [in]

An array of <a href="https://msdn.microsoft.com/d0c142a9-2495-46e6-b53b-0c415bddb0b2">WTSSBX_SESSION_INFO</a> structures that contain information about sessions. Only the members that have changed are reported in this structure. The others are set to zero.


## -returns



Returns <b>S_OK</b> if successful.




## -remarks



The <b>WTSSBX_SessionChangeNotification</b> method can report up to 25 sessions each time it is called. If Terminal Services Session Broker (TS Session Broker) needs to report more than 25 sessions, it calls this method multiple times until it reports all of its sessions.

Your implementation of this method must return <b>S_OK</b> immediately if successful.




## -see-also




<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

