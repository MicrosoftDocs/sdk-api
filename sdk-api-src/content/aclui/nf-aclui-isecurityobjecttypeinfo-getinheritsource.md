---
UID: NF:aclui.ISecurityObjectTypeInfo.GetInheritSource
title: ISecurityObjectTypeInfo::GetInheritSource (aclui.h)
description: The ISecurityObjectTypeInfo::GetInheritSource method provides a means of determining the source of inherited access control entries in discretionary access control lists and system access control lists.
helpviewer_keywords: ["GetInheritSource","GetInheritSource method [Security]","GetInheritSource method [Security]","ISecurityObjectTypeInfo interface","ISecurityObjectTypeInfo interface [Security]","GetInheritSource method","ISecurityObjectTypeInfo.GetInheritSource","ISecurityObjectTypeInfo::GetInheritSource","aclui/ISecurityObjectTypeInfo::GetInheritSource","security.isecurityobjecttypeinfo_getinheritsource"]
old-location: security\isecurityobjecttypeinfo_getinheritsource.htm
tech.root: security
ms.assetid: e058ca98-08dc-4a3f-9521-adcc5990eae7
ms.date: 12/05/2018
ms.keywords: GetInheritSource, GetInheritSource method [Security], GetInheritSource method [Security],ISecurityObjectTypeInfo interface, ISecurityObjectTypeInfo interface [Security],GetInheritSource method, ISecurityObjectTypeInfo.GetInheritSource, ISecurityObjectTypeInfo::GetInheritSource, aclui/ISecurityObjectTypeInfo::GetInheritSource, security.isecurityobjecttypeinfo_getinheritsource
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
 - ISecurityObjectTypeInfo::GetInheritSource
 - aclui/ISecurityObjectTypeInfo::GetInheritSource
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
 - ISecurityObjectTypeInfo.GetInheritSource
---

# ISecurityObjectTypeInfo::GetInheritSource


## -description

The <b>GetInheritSource</b> method provides a means of determining the source of inherited <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) in <a href="/windows/desktop/SecGloss/d-gly">discretionary access control lists</a> (DACLs) and <a href="/windows/desktop/SecGloss/s-gly">system access control lists</a> (SACLs).

## -parameters

### -param si [in]

A <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure that represents the security information of the object.

### -param pACL [in]

A pointer to an <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure that represents the <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL) of the object.

### -param ppInheritArray [out]

A pointer to a pointer to an <a href="/windows/desktop/api/accctrl/ns-accctrl-inherited_froma">INHERITED_FROM</a> structure that receives an array of <b>INHERITED_FROM</b> structures. The length of this array is the same as the number of <a href="/windows/desktop/SecAuthZ/ace">ACEs</a> in the ACL referenced by <i>pACL</i>. Each <b>INHERITED_FROM</b> entry in <i>ppInheritArray</i> provides inheritance information for the corresponding <b>ACE</b> entry in <i>pACL</i>.

## -returns

If the function is successful, the return value is S_OK.

 
If the function fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.