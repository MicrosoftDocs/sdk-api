---
UID: NE:evntcons.EVENTSECURITYOPERATION
title: EVENTSECURITYOPERATION (evntcons.h)
description: Defines what component of the security descriptor that the EventAccessControl function modifies.
helpviewer_keywords: ["EVENTSECURITYOPERATION","EVENTSECURITYOPERATION enumeration [ETW]","EventSecurityAddDACL","EventSecurityAddSACL","EventSecurityMax","EventSecuritySetDACL","EventSecuritySetSACL","base.eventsecurityoperation","etw.eventsecurityoperation","evntcons/EVENTSECURITYOPERATION","evntcons/EventSecurityAddDACL","evntcons/EventSecurityAddSACL","evntcons/EventSecurityMax","evntcons/EventSecuritySetDACL","evntcons/EventSecuritySetSACL"]
old-location: etw\eventsecurityoperation.htm
tech.root: ETW
ms.assetid: 81f6cf07-2705-4075-b085-d5aebba17121
ms.date: 12/05/2018
ms.keywords: EVENTSECURITYOPERATION, EVENTSECURITYOPERATION enumeration [ETW], EventSecurityAddDACL, EventSecurityAddSACL, EventSecurityMax, EventSecuritySetDACL, EventSecuritySetSACL, base.eventsecurityoperation, etw.eventsecurityoperation, evntcons/EVENTSECURITYOPERATION, evntcons/EventSecurityAddDACL, evntcons/EventSecurityAddSACL, evntcons/EventSecurityMax, evntcons/EventSecuritySetDACL, evntcons/EventSecuritySetSACL
req.header: evntcons.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EVENTSECURITYOPERATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EVENTSECURITYOPERATION
 - evntcons/EVENTSECURITYOPERATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntcons.h
api_name:
 - EVENTSECURITYOPERATION
---

# EVENTSECURITYOPERATION enumeration (evntcons.h)


## -description

Defines what component of the security descriptor that the <a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a> function modifies.

## -enum-fields

### -field EventSecuritySetDACL

Clears the current discretionary access control list (DACL) and adds an ACE to the DACL. The <i>Sid</i>, <i>Rights</i>, and <i>AllowOrDeny</i> parameters of the <a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a> function determine the contents of the ACE (who has access to the provider or session and the type of access). To add a new ACE to the DACL without clearing the existing DACL, specify EventSecurityAddDACL.

### -field EventSecuritySetSACL

Clears the current system access control list (SACL) and adds an audit ACE to the SACL. The <i>Sid</i> and <i>Rights</i> parameters of the <a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a> function determine the contents of the ACE (who generates an audit record when attempting the specified access). To add a new ACE to the SACL without clearing the existing SACL, specify EventSecurityAddSACL.

### -field EventSecurityAddDACL

Adds an ACE to the current DACL. The <i>Sid</i>, <i>Rights</i>, and <i>AllowOrDeny</i> parameters of the <a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a> function determine the contents of the ACE (who has access to the provider or session and the type of access).

### -field EventSecurityAddSACL

Adds an ACE to the current SACL. The <i>Sid</i> and <i>Rights</i> parameters of the <a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a> function determine the contents of the ACE (who generates an audit record when attempting the specified access).

### -field EventSecurityMax

Reserved.

## -remarks

For information on DACLs and SACLs, see <a href="/windows/desktop/SecAuthZ/access-control-lists">Access Control Lists</a>.

## -see-also

<a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a>

