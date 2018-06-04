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

# __MIDL___MIDL_itf_rdpencomapi_0000_0000_0002 enumeration


## -description


Defines values for the reasons why an attendee was disconnected from the session.


## -enum-fields




### -field ATTENDEE_DISCONNECT_REASON_MIN

Minimum enumeration value.


### -field ATTENDEE_DISCONNECT_REASON_APP

The application called the <a href="https://msdn.microsoft.com/e666fdd4-7417-40ea-9643-d7df587294f2">IRDPSRAPIAttendee::TerminateConnection</a> method.


### -field ATTENDEE_DISCONNECT_REASON_ERR

There was an internal error when processing data from an attendee or trying to manage an attendee


### -field ATTENDEE_DISCONNECT_REASON_CLI

The attendee disconnected after a request from the attendee itself.


### -field ATTENDEE_DISCONNECT_REASON_MAX

Maximum enumeration value.


## -see-also




<a href="https://msdn.microsoft.com/4445809f-1aad-4d76-9199-4d5246c7c83d">Reason Property of IRDPSRAPIAttendeeDisconnectInfo</a>
 

 

