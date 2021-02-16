---
UID: NS:winnt._SYSTEM_ALARM_CALLBACK_ACE
title: SYSTEM_ALARM_CALLBACK_ACE (winnt.h)
description: The SYSTEM_ALARM_CALLBACK_ACE structure is reserved for future use.
helpviewer_keywords: ["*PSYSTEM_ALARM_CALLBACK_ACE","SYSTEM_ALARM_CALLBACK_ACE","SYSTEM_ALARM_CALLBACK_ACE structure [Security]","security.system_alarm_callback_ace","winnt/SYSTEM_ALARM_CALLBACK_ACE"]
old-location: security\system_alarm_callback_ace.htm
tech.root: security
ms.assetid: 8bfb579f-4bee-454e-827b-63a800bccf85
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_ALARM_CALLBACK_ACE, SYSTEM_ALARM_CALLBACK_ACE, SYSTEM_ALARM_CALLBACK_ACE structure [Security], security.system_alarm_callback_ace, winnt/SYSTEM_ALARM_CALLBACK_ACE'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SYSTEM_ALARM_CALLBACK_ACE, *PSYSTEM_ALARM_CALLBACK_ACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_ALARM_CALLBACK_ACE
 - winnt/_SYSTEM_ALARM_CALLBACK_ACE
 - PSYSTEM_ALARM_CALLBACK_ACE
 - winnt/PSYSTEM_ALARM_CALLBACK_ACE
 - SYSTEM_ALARM_CALLBACK_ACE
 - winnt/SYSTEM_ALARM_CALLBACK_ACE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SYSTEM_ALARM_CALLBACK_ACE
---

# SYSTEM_ALARM_CALLBACK_ACE structure


## -description

Not supported.

The <b>SYSTEM_ALARM_CALLBACK_ACE</b> structure is reserved for future use.

## -struct-fields

### -field Header

<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure that specifies the size and type of ACE. It also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to SYSTEM_ALARM_CALLBACK_ACE_TYPE.

### -field Mask

Specifies an 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> structure that gives the access rights that cause audit messages to be generated. The SUCCESSFUL_ACCESS_ACE_FLAG and FAILED_ACCESS_ACE_FLAG flags in the <b>AceFlags</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure indicate whether messages are generated for successful access attempts, unsuccessful access attempts, or both.

### -field SidStart

The first <b>DWORD</b> of a trustee's ACE. This ACE can be appended with application data. When the <a href="/windows/desktop/SecAuthZ/authzaccesscheckcallback">AuthzAccessCheckCallback</a> function is called, this ACE is passed as the <i>pAce</i> parameter of that function.

## -remarks

ACE structures must be aligned on <b>DWORD</b> boundaries. All Windows memory-management functions return <b>DWORD</b>-aligned handles to memory.