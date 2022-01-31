---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0001
title: CTRL_LEVEL (rdpencomapi.h)
description: Defines the level of control that an attendee has on a session.
helpviewer_keywords: ["CTRL_LEVEL","CTRL_LEVEL enumeration [RDP]","CTRL_LEVEL_INTERACTIVE","CTRL_LEVEL_INVALID","CTRL_LEVEL_MAX","CTRL_LEVEL_MIN","CTRL_LEVEL_NONE","CTRL_LEVEL_REQCTRL_INTERACTIVE","CTRL_LEVEL_REQCTRL_VIEW","CTRL_LEVEL_VIEW","rdp.ctrl_level","rdpencomapi/CTRL_LEVEL","rdpencomapi/CTRL_LEVEL_INTERACTIVE","rdpencomapi/CTRL_LEVEL_INVALID","rdpencomapi/CTRL_LEVEL_MAX","rdpencomapi/CTRL_LEVEL_MIN","rdpencomapi/CTRL_LEVEL_NONE","rdpencomapi/CTRL_LEVEL_REQCTRL_INTERACTIVE","rdpencomapi/CTRL_LEVEL_REQCTRL_VIEW","rdpencomapi/CTRL_LEVEL_VIEW"]
old-location: rdp\ctrl_level.htm
tech.root: rdp
ms.assetid: f97b0493-82bf-487e-adc1-2dc40eeeb36c
ms.date: 12/05/2018
ms.keywords: CTRL_LEVEL, CTRL_LEVEL enumeration [RDP], CTRL_LEVEL_INTERACTIVE, CTRL_LEVEL_INVALID, CTRL_LEVEL_MAX, CTRL_LEVEL_MIN, CTRL_LEVEL_NONE, CTRL_LEVEL_REQCTRL_INTERACTIVE, CTRL_LEVEL_REQCTRL_VIEW, CTRL_LEVEL_VIEW, rdp.ctrl_level, rdpencomapi/CTRL_LEVEL, rdpencomapi/CTRL_LEVEL_INTERACTIVE, rdpencomapi/CTRL_LEVEL_INVALID, rdpencomapi/CTRL_LEVEL_MAX, rdpencomapi/CTRL_LEVEL_MIN, rdpencomapi/CTRL_LEVEL_NONE, rdpencomapi/CTRL_LEVEL_REQCTRL_INTERACTIVE, rdpencomapi/CTRL_LEVEL_REQCTRL_VIEW, rdpencomapi/CTRL_LEVEL_VIEW
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rdpencomapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CTRL_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_rdpencomapi_0000_0000_0001
 - rdpencomapi/__MIDL___MIDL_itf_rdpencomapi_0000_0000_0001
 - CTRL_LEVEL
 - rdpencomapi/CTRL_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rdpencomapi.h
api_name:
 - CTRL_LEVEL
---

# CTRL_LEVEL enumeration


## -description

Defines the level of control that an attendee has on a session.

## -enum-fields

### -field CTRL_LEVEL_MIN:0

Minimum enumeration value.

### -field CTRL_LEVEL_INVALID:0

The control level is not valid.

### -field CTRL_LEVEL_NONE:1

The attendee cannot view or interact with the session. This is the default.

### -field CTRL_LEVEL_VIEW:2

The attendee can view the session.

### -field CTRL_LEVEL_INTERACTIVE:3

The attendee can view and interact with the session. The local keyboard and mouse input is redirected to 
      the session.

### -field CTRL_LEVEL_REQCTRL_VIEW:4

The attendee can view the session.

<b>Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This enumeration value is not supported.

### -field CTRL_LEVEL_REQCTRL_INTERACTIVE:5

The attendee can view and interact with the session. The local keyboard and mouse input is redirected to the 
       session. Hosting applications that want to allow users to control the shared session must either define 
       <b>uiAccess</b> as "true" in their application manifest OR run at High Integrity 
       Level (elevated). For more information see 
       <a href="/windows/desktop/WinAuto/uiauto-securityoverview">Setting UIAccess in the Application Manifest File</a>.

<b>Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This enumeration value is not supported.

### -field CTRL_LEVEL_MAX:5

Maximum enumeration value.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiattendee-get_controllevel">ControlLevel Property of IRDPSRAPIAttendee</a>



<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiviewer-requestcontrol">IRDPSRAPIViewer::RequestControl</a>



<a href="/previous-versions/windows/desktop/rdp/oncontrollevelchangerequest">OnControlLevelChangeRequest</a>
