---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0002
title: "__MIDL___MIDL_itf_rdpencomapi_0000_0000_0002"
author: windows-sdk-content
description: Defines values for the reasons why an attendee was disconnected from the session.
old-location: rdp\attendee_disconnect_reason.htm
old-project: Rdp
ms.assetid: 2fbe5df8-54da-49b2-a9b8-275e838c6d39
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: ATTENDEE_DISCONNECT_REASON, ATTENDEE_DISCONNECT_REASON enumeration [RDP], ATTENDEE_DISCONNECT_REASON_APP, ATTENDEE_DISCONNECT_REASON_CLI, ATTENDEE_DISCONNECT_REASON_ERR, ATTENDEE_DISCONNECT_REASON_MAX, ATTENDEE_DISCONNECT_REASON_MIN, __MIDL___MIDL_itf_rdpencomapi_0000_0000_0002, rdp.attendee_disconnect_reason, rdpencomapi/ATTENDEE_DISCONNECT_REASON, rdpencomapi/ATTENDEE_DISCONNECT_REASON_APP, rdpencomapi/ATTENDEE_DISCONNECT_REASON_CLI, rdpencomapi/ATTENDEE_DISCONNECT_REASON_ERR, rdpencomapi/ATTENDEE_DISCONNECT_REASON_MAX, rdpencomapi/ATTENDEE_DISCONNECT_REASON_MIN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rdpencomapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsTscAx.dll
tech.root: 
req.typenames: ATTENDEE_DISCONNECT_REASON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rdpencomapi.h
api_name:
 - ATTENDEE_DISCONNECT_REASON
product: Windows
targetos: Windows
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

