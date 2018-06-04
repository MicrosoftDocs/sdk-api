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
 

 

