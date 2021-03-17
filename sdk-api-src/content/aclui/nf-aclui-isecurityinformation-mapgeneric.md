---
UID: NF:aclui.ISecurityInformation.MapGeneric
title: ISecurityInformation::MapGeneric (aclui.h)
description: The MapGeneric method requests that the generic access rights in an access mask be mapped to their corresponding standard and specific access rights.
helpviewer_keywords: ["ISecurityInformation interface [Security]","MapGeneric method","ISecurityInformation.MapGeneric","ISecurityInformation::MapGeneric","MapGeneric","MapGeneric method [Security]","MapGeneric method [Security]","ISecurityInformation interface","_win32_isecurityinformation_mapgeneric","aclui/ISecurityInformation::MapGeneric","security.isecurityinformation_mapgeneric"]
old-location: security\isecurityinformation_mapgeneric.htm
tech.root: security
ms.assetid: 85ad4d42-11e7-4d26-943f-3d7451899c8e
ms.date: 12/05/2018
ms.keywords: ISecurityInformation interface [Security],MapGeneric method, ISecurityInformation.MapGeneric, ISecurityInformation::MapGeneric, MapGeneric, MapGeneric method [Security], MapGeneric method [Security],ISecurityInformation interface, _win32_isecurityinformation_mapgeneric, aclui/ISecurityInformation::MapGeneric, security.isecurityinformation_mapgeneric
req.header: aclui.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISecurityInformation::MapGeneric
 - aclui/ISecurityInformation::MapGeneric
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation.MapGeneric
---

# ISecurityInformation::MapGeneric


## -description

The <b>MapGeneric</b> method requests that the generic access rights in an <a href="/windows/desktop/SecGloss/a-gly">access mask</a> be mapped to their corresponding standard and specific access rights. For more information about generic, standard, and specific access rights, see 
<a href="/windows/desktop/SecAuthZ/access-rights-and-access-masks">Access Rights and Access Masks</a>.

## -parameters

### -param pguidObjectType [in]

A pointer to a 
<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies the type of object to which the <a href="/windows/desktop/SecGloss/a-gly">access mask</a> applies. If this member is <b>NULL</b> or a pointer to GUID_NULL, the access mask applies to the object itself.

### -param pAceFlags [in]

A pointer to the <b>AceFlags</b> member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure from the ACE whose access mask is being mapped.

### -param pMask [in]

A pointer to an access mask that contains the generic access rights to map. Your implementation must map the generic access rights to the corresponding standard and specific access rights for the specified object type.

## -returns

If the function succeeds, the function returns S_OK.

 If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Your <b>MapGeneric</b> implementation can call the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a> function to map the generic access rights in the access mask.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a>



<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a>



<a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>