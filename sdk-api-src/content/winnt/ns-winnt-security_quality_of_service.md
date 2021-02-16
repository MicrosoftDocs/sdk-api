---
UID: NS:winnt._SECURITY_QUALITY_OF_SERVICE
title: SECURITY_QUALITY_OF_SERVICE (winnt.h)
description: Contains information used to support client impersonation.
helpviewer_keywords: ["*PSECURITY_QUALITY_OF_SERVICE","PSECURITY_QUALITY_OF_SERVICE","PSECURITY_QUALITY_OF_SERVICE structure pointer [Security]","SECURITY_QUALITY_OF_SERVICE","SECURITY_QUALITY_OF_SERVICE structure [Security]","_SECURITY_QUALITY_OF_SERVICE","_win32_security_quality_of_service_str","security.security_quality_of_service","winnt/PSECURITY_QUALITY_OF_SERVICE","winnt/SECURITY_QUALITY_OF_SERVICE"]
old-location: security\security_quality_of_service.htm
tech.root: security
ms.assetid: 21f99d04-b21b-442c-9034-35f9f7bbee53
ms.date: 12/05/2018
ms.keywords: '*PSECURITY_QUALITY_OF_SERVICE, PSECURITY_QUALITY_OF_SERVICE, PSECURITY_QUALITY_OF_SERVICE structure pointer [Security], SECURITY_QUALITY_OF_SERVICE, SECURITY_QUALITY_OF_SERVICE structure [Security], _SECURITY_QUALITY_OF_SERVICE, _win32_security_quality_of_service_str, security.security_quality_of_service, winnt/PSECURITY_QUALITY_OF_SERVICE, winnt/SECURITY_QUALITY_OF_SERVICE'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SECURITY_QUALITY_OF_SERVICE, *PSECURITY_QUALITY_OF_SERVICE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECURITY_QUALITY_OF_SERVICE
 - winnt/_SECURITY_QUALITY_OF_SERVICE
 - PSECURITY_QUALITY_OF_SERVICE
 - winnt/PSECURITY_QUALITY_OF_SERVICE
 - SECURITY_QUALITY_OF_SERVICE
 - winnt/SECURITY_QUALITY_OF_SERVICE
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
 - SECURITY_QUALITY_OF_SERVICE
---

# SECURITY_QUALITY_OF_SERVICE structure


## -description

The <b>SECURITY_QUALITY_OF_SERVICE</b> data structure contains information used to support client impersonation. A client can specify this information when it connects to a server; the information determines whether the server may impersonate the client, and if so, to what extent.

## -struct-fields

### -field Length

Specifies the size, in bytes, of this structure.

### -field ImpersonationLevel

Specifies the information given to the server about the client, and how the server may represent, or impersonate, the client. Security impersonation levels govern the degree to which a server process can act on behalf of a client <a href="/windows/desktop/SecGloss/p-gly">process</a>. This member is a 
<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> enumeration type value.

### -field ContextTrackingMode

Specifies whether the server is to be given a snapshot of the client's <a href="/windows/desktop/SecGloss/s-gly">security context</a> (called static tracking), or is to be continually updated to track changes to the client's security context (called dynamic tracking). The SECURITY_STATIC_TRACKING value  specifies static tracking, and the SECURITY_DYNAMIC_TRACKING value specifies dynamic tracking. Not all communications mechanisms support dynamic tracking; those that do not will default to static tracking.

### -field EffectiveOnly

Specifies whether the server may enable or disable <a href="/windows/desktop/SecGloss/p-gly">privileges</a> and groups that the client's security context may include.

## -see-also

<a href="/windows/desktop/api/dde/nf-dde-ddesetqualityofservice">DdeSetQualityOfService</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>