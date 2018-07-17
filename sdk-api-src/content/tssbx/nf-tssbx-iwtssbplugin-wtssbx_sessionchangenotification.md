---
UID: NF:tssbx.IWTSSBPlugin.WTSSBX_SessionChangeNotification
title: IWTSSBPlugin::WTSSBX_SessionChangeNotification
author: windows-sdk-content
description: Notifies the plug-in that a change, such as a logon, logoff, disconnect, or reconnect, occurred in the session.
old-location: termserv\iwtssbplugin_wtssbx_sessionchangenotification.htm
old-project: termserv
ms.assetid: 00426aa2-1d22-462f-9ad1-2a63d151493d
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: IWTSSBPlugin interface [Remote Desktop Services],WTSSBX_SessionChangeNotification method, IWTSSBPlugin.WTSSBX_SessionChangeNotification, IWTSSBPlugin::WTSSBX_SessionChangeNotification, WTSSBX_SessionChangeNotification, WTSSBX_SessionChangeNotification method [Remote Desktop Services], WTSSBX_SessionChangeNotification method [Remote Desktop Services],IWTSSBPlugin interface, termserv.iwtssbplugin_wtssbx_sessionchangenotification, tssbx/IWTSSBPlugin::WTSSBX_SessionChangeNotification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTSSBX_NOTIFICATION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tssbx.h
api_name:
 - IWTSSBPlugin.WTSSBX_SessionChangeNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

