---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0001
title: "__MIDL___MIDL_itf_rdpencomapi_0000_0000_0001"
author: windows-driver-content
description: Defines the level of control that an attendee has on a session.
old-location: rdp\ctrl_level.htm
old-project: Rdp
ms.assetid: f97b0493-82bf-487e-adc1-2dc40eeeb36c
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: CTRL_LEVEL, CTRL_LEVEL enumeration [RDP], CTRL_LEVEL_INTERACTIVE, CTRL_LEVEL_INVALID, CTRL_LEVEL_MAX, CTRL_LEVEL_MIN, CTRL_LEVEL_NONE, CTRL_LEVEL_REQCTRL_INTERACTIVE, CTRL_LEVEL_REQCTRL_VIEW, CTRL_LEVEL_VIEW, __MIDL___MIDL_itf_rdpencomapi_0000_0000_0001, rdp.ctrl_level, rdpencomapi/CTRL_LEVEL, rdpencomapi/CTRL_LEVEL_INTERACTIVE, rdpencomapi/CTRL_LEVEL_INVALID, rdpencomapi/CTRL_LEVEL_MAX, rdpencomapi/CTRL_LEVEL_MIN, rdpencomapi/CTRL_LEVEL_NONE, rdpencomapi/CTRL_LEVEL_REQCTRL_INTERACTIVE, rdpencomapi/CTRL_LEVEL_REQCTRL_VIEW, rdpencomapi/CTRL_LEVEL_VIEW
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CTRL_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rdpencomapi.h
api_name:
-	CTRL_LEVEL
product: Windows
targetos: Windows
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_rdpencomapi_0000_0000_0001 enumeration


## -description


Defines the level of control that an attendee has on a session.


## -enum-fields




### -field CTRL_LEVEL_MIN

Minimum enumeration value.


### -field CTRL_LEVEL_INVALID

The control level is not valid.


### -field CTRL_LEVEL_NONE

The attendee cannot view or interact with the session. This is the default.


### -field CTRL_LEVEL_VIEW

The attendee can view the session.


### -field CTRL_LEVEL_INTERACTIVE

The attendee can view and interact with the session. The local keyboard and mouse input is redirected to 
      the session.


### -field CTRL_LEVEL_REQCTRL_VIEW

The attendee can view the session.

<b>Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This enumeration value is not supported.


### -field CTRL_LEVEL_REQCTRL_INTERACTIVE

The attendee can view and interact with the session. The local keyboard and mouse input is redirected to the 
       session. Hosting applications that want to allow users to control the shared session must either define 
       <b>uiAccess</b> as "true" in their application manifest OR run at High Integrity 
       Level (elevated). For more information see 
       <a href="https://msdn.microsoft.com/0c3689e1-2124-4142-b0bd-233e95ee1285">Setting UIAccess in the Application Manifest File</a>.

<b>Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This enumeration value is not supported.


### -field CTRL_LEVEL_MAX

Maximum enumeration value.


## -see-also




<a href="https://msdn.microsoft.com/b154580d-f541-4668-9255-607ab2de46a9">ControlLevel Property of IRDPSRAPIAttendee</a>



<a href="https://msdn.microsoft.com/be913f3c-9a5b-46bd-be9a-1ba0b0c20211">IRDPSRAPIViewer::RequestControl</a>



<a href="https://msdn.microsoft.com/24021ff3-6dde-40c4-9dac-279442bd085d">OnControlLevelChangeRequest</a>
 

 

