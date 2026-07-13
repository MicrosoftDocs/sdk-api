---
UID: NF:aclapi.LookupSecurityDescriptorPartsW
title: LookupSecurityDescriptorPartsW function (aclapi.h)
description: Retrieves security information from a self-relative security descriptor. (Unicode)
helpviewer_keywords: ["LookupSecurityDescriptorParts", "LookupSecurityDescriptorParts function [Security]", "LookupSecurityDescriptorPartsW", "_win32_lookupsecuritydescriptorparts", "aclapi/LookupSecurityDescriptorParts", "aclapi/LookupSecurityDescriptorPartsW", "security.lookupsecuritydescriptorparts"]
old-location: security\lookupsecuritydescriptorparts.htm
tech.root: security
ms.assetid: 68c3f56b-6c48-4f4b-bd38-9f4e346c663b
ms.date: 12/05/2018
ms.keywords: LookupSecurityDescriptorParts, LookupSecurityDescriptorParts function [Security], LookupSecurityDescriptorPartsA, LookupSecurityDescriptorPartsW, _win32_lookupsecuritydescriptorparts, aclapi/LookupSecurityDescriptorParts, aclapi/LookupSecurityDescriptorPartsA, aclapi/LookupSecurityDescriptorPartsW, security.lookupsecuritydescriptorparts
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LookupSecurityDescriptorPartsW (Unicode) and LookupSecurityDescriptorPartsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LookupSecurityDescriptorPartsW
 - aclapi/LookupSecurityDescriptorPartsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - LookupSecurityDescriptorParts
 - LookupSecurityDescriptorPartsA
 - LookupSecurityDescriptorPartsW
---

# LookupSecurityDescriptorPartsW function


## -description

The <b>LookupSecurityDescriptorParts</b> function retrieves security information from a <a href="/windows/desktop/SecGloss/s-gly">self-relative security descriptor</a>.

## -parameters

### -param ppOwner [out, optional]

A pointer to a variable that receives a pointer to a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure. The function looks up the name associated with the owner 
<a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID)  in the <i>pSD</i> <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>, and returns a pointer to the name in the <b>ptstrName</b> member of the <b>TRUSTEE</b> structure. The function sets the <b>TrusteeForm</b> member to TRUSTEE_IS_NAME. 




This parameter can be <b>NULL</b> if you are not interested in the name of the owner.

### -param ppGroup [out, optional]

A pointer to a variable that receives a pointer to a <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure. The function looks up the name associated with the primary group SID of the security descriptor, and returns a pointer to the name in the <b>ptstrName</b> member of the <b>TRUSTEE</b> structure. The function sets the <b>TrusteeForm</b> member to TRUSTEE_IS_NAME.  




This parameter can be <b>NULL</b> if you are not interested in the name of the group.

### -param pcCountOfAccessEntries [out, optional]

A pointer to a <b>ULONG</b> that receives the number of 
<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structures returned in the <i>pListOfAccessEntries</i> array. This parameter can be <b>NULL</b> only if the <i>pListOfAccessEntries</i> parameter is also <b>NULL</b>.

### -param ppListOfAccessEntries [out, optional]

A pointer to a variable that receives a pointer to an array of <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structures that describe the <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) in the <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) of the security descriptor. The 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure in these <b>EXPLICIT_ACCESS</b> structures use the TRUSTEE_IS_NAME form. For a description of how an array of <b>EXPLICIT_ACCESS</b> structures describes the ACEs in an 
<a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL), see the 
<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a> function. If this parameter is <b>NULL</b>, the <i>cCountOfAccessEntries</i> parameter must also be <b>NULL</b>.

### -param pcCountOfAuditEntries [out, optional]

A pointer to a <b>ULONG</b> that receives the number of <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structures returned in the <i>pListOfAuditEntries</i> array. This parameter can be <b>NULL</b> only if the <i>pListOfAuditEntries</i> parameter is also <b>NULL</b>.

### -param ppListOfAuditEntries [out, optional]

A pointer to a variable that receives a pointer to an array of <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structures that describe the ACEs in the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) of the security descriptor. The <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure in these <b>EXPLICIT_ACCESS</b> structures uses the TRUSTEE_IS_NAME form. If this parameter is <b>NULL</b>, the <i>cCountOfAuditEntries</i> parameter must also be <b>NULL</b>.

### -param pSD [in]

A pointer to an existing <a href="/windows/desktop/SecGloss/s-gly">self-relative security descriptor</a> from which the function retrieves security information.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.

## -remarks

The <b>LookupSecurityDescriptorParts</b> function retrieves the names of the owner and primary group of the security descriptor. This function also returns descriptions of the ACEs in the DACL and audit-control entries in the SACL of the security descriptor.

The parameters other than <i>pSD</i> can be <b>NULL</b> if you are not interested in the information. If you do not want information about the DACL, both <i>pListOfAccessEntries</i> and <i>cCountOfAuditEntries</i> must be <b>NULL</b>. If you do not want information about the SACL, both <i>pListOfAuditEntries</i> and <i>cCountOfAuditEntries</i> must be <b>NULL</b>. Similarly, if you do want DACL or SACL information, both of the corresponding parameters must not be <b>NULL</b>.

When you have finished using any of the buffers returned by the <i>pOwner</i>, <i>pGroup</i>, <i>pListOfAccessEntries</i>, or <i>pListOfAuditEntries</i> parameters, free them by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

The <b>LookupSecurityDescriptorParts</b> function is intended for trusted servers that implement or expose security on their own objects. The function works with a self-relative security descriptor suitable for serializing into a stream and storing to disk, as a trusted server might require.





> [!NOTE]
> The aclapi.h header defines LookupSecurityDescriptorParts as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/ace">ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>
