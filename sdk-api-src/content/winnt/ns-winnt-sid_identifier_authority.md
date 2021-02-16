---
UID: NS:winnt._SID_IDENTIFIER_AUTHORITY
title: SID_IDENTIFIER_AUTHORITY (winnt.h)
description: Represents the top-level authority of a security identifier (SID).
helpviewer_keywords: ["*PSID_IDENTIFIER_AUTHORITY","PSID_IDENTIFIER_AUTHORITY","PSID_IDENTIFIER_AUTHORITY structure pointer [Security]","SID_IDENTIFIER_AUTHORITY","SID_IDENTIFIER_AUTHORITY structure [Security]","_SID_IDENTIFIER_AUTHORITY","_win32_sid_identifier_authority_str","security.sid_identifier_authority","winnt/PSID_IDENTIFIER_AUTHORITY","winnt/SID_IDENTIFIER_AUTHORITY"]
old-location: security\sid_identifier_authority.htm
tech.root: security
ms.assetid: 450a6d2d-d2e4-4098-90af-a8024ddcfcb5
ms.date: 12/05/2018
ms.keywords: '*PSID_IDENTIFIER_AUTHORITY, PSID_IDENTIFIER_AUTHORITY, PSID_IDENTIFIER_AUTHORITY structure pointer [Security], SID_IDENTIFIER_AUTHORITY, SID_IDENTIFIER_AUTHORITY structure [Security], _SID_IDENTIFIER_AUTHORITY, _win32_sid_identifier_authority_str, security.sid_identifier_authority, winnt/PSID_IDENTIFIER_AUTHORITY, winnt/SID_IDENTIFIER_AUTHORITY'
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
req.typenames: SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SID_IDENTIFIER_AUTHORITY
 - winnt/_SID_IDENTIFIER_AUTHORITY
 - PSID_IDENTIFIER_AUTHORITY
 - winnt/PSID_IDENTIFIER_AUTHORITY
 - SID_IDENTIFIER_AUTHORITY
 - winnt/SID_IDENTIFIER_AUTHORITY
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
 - SID_IDENTIFIER_AUTHORITY
---

# SID_IDENTIFIER_AUTHORITY structure


## -description

The <b>SID_IDENTIFIER_AUTHORITY</b> structure represents the top-level authority of a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

## -struct-fields

### -field Value

An array of 6 bytes specifying a SID's top-level authority.

## -remarks

The identifier authority value identifies the agency that issued the SID. The following identifier authorities are predefined.

<table>
<tr>
<th>Identifier authority</th>
<th>Value</th>
</tr>
<tr>
<td>SECURITY_NULL_SID_AUTHORITY</td>
<td>0</td>
</tr>
<tr>
<td>SECURITY_WORLD_SID_AUTHORITY</td>
<td>1</td>
</tr>
<tr>
<td>SECURITY_LOCAL_SID_AUTHORITY</td>
<td>2</td>
</tr>
<tr>
<td>SECURITY_CREATOR_SID_AUTHORITY</td>
<td>3</td>
</tr>
<tr>
<td>SECURITY_NON_UNIQUE_AUTHORITY</td>
<td>4</td>
</tr>
<tr>
<td>SECURITY_NT_AUTHORITY</td>
<td>5</td>
</tr>
<tr>
<td>SECURITY_RESOURCE_MANAGER_AUTHORITY</td>
<td>9</td>
</tr>
</table>
 

A SID must contain a top-level authority and at least one <a href="/windows/desktop/SecGloss/r-gly">relative identifier</a> (RID) value.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority">GetSidIdentifierAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesid">InitializeSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>