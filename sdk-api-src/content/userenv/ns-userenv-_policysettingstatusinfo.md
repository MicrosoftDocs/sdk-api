---
UID: NS:userenv._POLICYSETTINGSTATUSINFO
title: "_POLICYSETTINGSTATUSINFO"
author: windows-sdk-content
description: The POLICYSETTINGSTATUSINFO structure provides information about a policy-setting event.
old-location: policy\policysettingstatusinfo_str.htm
tech.root: Policy
ms.assetid: f86dbd35-9180-43f1-ad66-7dba31e1fc89
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPPOLICYSETTINGSTATUSINFO, LPPOLICYSETTINGSTATUSINFO, LPPOLICYSETTINGSTATUSINFO structure pointer [Group Policy], POLICYSETTINGSTATUSINFO, POLICYSETTINGSTATUSINFO structure [Group Policy], RSOPApplied, RSOPFailed, RSOPIgnored, RSOPSubsettingFailed, RSOPUnspecified, _POLICYSETTINGSTATUSINFO, _win32_policysettingstatusinfo_str, policy.policysettingstatusinfo_str, userenv/LPPOLICYSETTINGSTATUSINFO, userenv/POLICYSETTINGSTATUSINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Userenv.h
api_name:
 - POLICYSETTINGSTATUSINFO
product: Windows
targetos: Windows
req.typenames: POLICYSETTINGSTATUSINFO, *LPPOLICYSETTINGSTATUSINFO
req.redist: 
---

# _POLICYSETTINGSTATUSINFO structure


## -description


The
    <b>POLICYSETTINGSTATUSINFO</b> structure provides information about a policy-setting event.


## -struct-fields




### -field szKey

This member is optional. If it is <b>NULL</b>, the system generates a value.


### -field szEventSource

Pointer to a string specifying the name of the source (application, service, driver, subsystem) that generated the log entry.


### -field szEventLogName

Pointer to a string specifying the name of the event log.


### -field dwEventID

Specifies the event log message ID.


### -field dwErrorCode

A 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> that indicates an error that occurred during the application of the policy setting.


### -field status

Specifies the status of the policy setting. This member can be one of the following values.



#### RSOPUnspecified

The client-side extension does not define a status for this policy setting.



#### RSOPApplied

The policy setting was applied successfully.



#### RSOPIgnored

The policy setting was ignored; the system made no attempt to apply it.



#### RSOPFailed

Application of the policy setting failed. Details about the failure are indicated by the other members of the structure.



#### RSOPSubsettingFailed

The policy setting was applied successfully, but an error occurred while attempting to apply the child setting.


### -field timeLogged

Specifies a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that indicates the time at which the source generated the event.


## -see-also




<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>



<a href="https://msdn.microsoft.com/7ea2f217-4dd2-4c0f-af1b-d4bcb8707519">RSoPSetPolicySettingStatus</a>
 

 

