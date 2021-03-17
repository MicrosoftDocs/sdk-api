---
UID: NS:winnt._TOKEN_ACCESS_INFORMATION
title: TOKEN_ACCESS_INFORMATION (winnt.h)
description: Specifies all the information in a token that is necessary to perform an access check.
helpviewer_keywords: ["*PTOKEN_ACCESS_INFORMATION","PTOKEN_ACCESS_INFORMATION","PTOKEN_ACCESS_INFORMATION structure pointer [Security]","TOKEN_ACCESS_INFORMATION","TOKEN_ACCESS_INFORMATION structure [Security]","_TOKEN_ACCESS_INFORMATION","security.token_access_information","winnt/PTOKEN_ACCESS_INFORMATION","winnt/TOKEN_ACCESS_INFORMATION"]
old-location: security\token_access_information.htm
tech.root: security
ms.assetid: cb727b91-c88f-48f3-8329-020d3f727dc7
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_ACCESS_INFORMATION, PTOKEN_ACCESS_INFORMATION, PTOKEN_ACCESS_INFORMATION structure pointer [Security], TOKEN_ACCESS_INFORMATION, TOKEN_ACCESS_INFORMATION structure [Security], _TOKEN_ACCESS_INFORMATION, security.token_access_information, winnt/PTOKEN_ACCESS_INFORMATION, winnt/TOKEN_ACCESS_INFORMATION'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: TOKEN_ACCESS_INFORMATION, *PTOKEN_ACCESS_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_ACCESS_INFORMATION
 - winnt/_TOKEN_ACCESS_INFORMATION
 - PTOKEN_ACCESS_INFORMATION
 - winnt/PTOKEN_ACCESS_INFORMATION
 - TOKEN_ACCESS_INFORMATION
 - winnt/TOKEN_ACCESS_INFORMATION
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
 - TOKEN_ACCESS_INFORMATION
---

# TOKEN_ACCESS_INFORMATION structure


## -description

The <b>TOKEN_ACCESS_INFORMATION</b> structure specifies all the information in a token that is necessary to perform an access check.<div class="alert"><b>Note</b>  This structure doesn't contain token claim information. Applications that support conditional expression <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) should not use this structure for verifying access. For information about access validation support for conditional expressions, see the <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> and <a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a> functions.</div>
<div> </div>

## -struct-fields

### -field SidHash

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes_hash">SID_AND_ATTRIBUTES_HASH</a> structure that specifies a hash of the token's <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

### -field RestrictedSidHash

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes_hash">SID_AND_ATTRIBUTES_HASH</a> structure that specifies a hash of the token's restricted SID.

### -field Privileges

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a> structure that specifies information about the token's privileges.

### -field AuthenticationId

A <a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure that specifies the token's identity.

### -field TokenType

A value of the <a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a> enumeration that specifies the token's type.

### -field ImpersonationLevel

A value of the <a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> enumeration that specifies the token's impersonation level.

### -field MandatoryPolicy

A <a href="/windows/desktop/api/winnt/ns-winnt-token_mandatory_policy">TOKEN_MANDATORY_POLICY</a> structure that specifies the token's mandatory integrity policy.

### -field Flags

Reserved. Must be set to zero.

### -field AppContainerNumber

The app container number for the token or zero if this is not an app container token.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This member is not available.

### -field PackageSid

The app container SID or <b>NULL</b> if this is not an app container token.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This member is not available.

### -field CapabilitiesHash

Pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes_hash">SID_AND_ATTRIBUTES_HASH</a> structure that specifies a hash of the token's capability SIDs.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This member is not available.

### -field TrustLevelSid

The protected process trust level of the token.

### -field SecurityAttributes

Reserved. Must be set to <b>NULL</b>.

<b>Prior to Windows 10:  </b>This member is not available.

## -see-also

<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>