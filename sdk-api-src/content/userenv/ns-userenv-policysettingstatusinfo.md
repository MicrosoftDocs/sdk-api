---
UID: NS:userenv._POLICYSETTINGSTATUSINFO
title: POLICYSETTINGSTATUSINFO (userenv.h)
description: The POLICYSETTINGSTATUSINFO structure provides information about a policy-setting event.
helpviewer_keywords: ["*LPPOLICYSETTINGSTATUSINFO","LPPOLICYSETTINGSTATUSINFO","LPPOLICYSETTINGSTATUSINFO structure pointer [Group Policy]","POLICYSETTINGSTATUSINFO","POLICYSETTINGSTATUSINFO structure [Group Policy]","RSOPApplied","RSOPFailed","RSOPIgnored","RSOPSubsettingFailed","RSOPUnspecified","_win32_policysettingstatusinfo_str","policy.policysettingstatusinfo_str","userenv/LPPOLICYSETTINGSTATUSINFO","userenv/POLICYSETTINGSTATUSINFO"]
old-location: policy\policysettingstatusinfo_str.htm
tech.root: Policy
ms.assetid: f86dbd35-9180-43f1-ad66-7dba31e1fc89
ms.date: 12/05/2018
ms.keywords: '*LPPOLICYSETTINGSTATUSINFO, LPPOLICYSETTINGSTATUSINFO, LPPOLICYSETTINGSTATUSINFO structure pointer [Group Policy], POLICYSETTINGSTATUSINFO, POLICYSETTINGSTATUSINFO structure [Group Policy], RSOPApplied, RSOPFailed, RSOPIgnored, RSOPSubsettingFailed, RSOPUnspecified, _win32_policysettingstatusinfo_str, policy.policysettingstatusinfo_str, userenv/LPPOLICYSETTINGSTATUSINFO, userenv/POLICYSETTINGSTATUSINFO'
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
targetos: Windows
req.typenames: POLICYSETTINGSTATUSINFO, *LPPOLICYSETTINGSTATUSINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICYSETTINGSTATUSINFO
 - userenv/_POLICYSETTINGSTATUSINFO
 - LPPOLICYSETTINGSTATUSINFO
 - userenv/LPPOLICYSETTINGSTATUSINFO
 - POLICYSETTINGSTATUSINFO
 - userenv/POLICYSETTINGSTATUSINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Userenv.h
api_name:
 - POLICYSETTINGSTATUSINFO
---

# POLICYSETTINGSTATUSINFO structure


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
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> that indicates an error that occurred during the application of the policy setting.

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
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that indicates the time at which the source generated the event.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-structures">Group Policy Structures</a>



<a href="/windows/desktop/api/userenv/nf-userenv-rsopsetpolicysettingstatus">RSoPSetPolicySettingStatus</a>