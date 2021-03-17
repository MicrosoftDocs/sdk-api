---
UID: NF:aclui.ISecurityInformation2.IsDaclCanonical
title: ISecurityInformation2::IsDaclCanonical (aclui.h)
description: The IsDaclCanonical method determines whether the ACEs contained in the specified DACL structure are ordered according to the definition of DACL ordering implemented by the client.
helpviewer_keywords: ["ISecurityInformation2 interface [Security]","IsDaclCanonical method","ISecurityInformation2.IsDaclCanonical","ISecurityInformation2::IsDaclCanonical","IsDaclCanonical","IsDaclCanonical method [Security]","IsDaclCanonical method [Security]","ISecurityInformation2 interface","_win32_isecurityinformation2_isdaclcanonical","aclui/ISecurityInformation2::IsDaclCanonical","security.isecurityinformation2_isdaclcanonical"]
old-location: security\isecurityinformation2_isdaclcanonical.htm
tech.root: security
ms.assetid: 54b83592-0cfb-45db-9788-05459c9ec35c
ms.date: 12/05/2018
ms.keywords: ISecurityInformation2 interface [Security],IsDaclCanonical method, ISecurityInformation2.IsDaclCanonical, ISecurityInformation2::IsDaclCanonical, IsDaclCanonical, IsDaclCanonical method [Security], IsDaclCanonical method [Security],ISecurityInformation2 interface, _win32_isecurityinformation2_isdaclcanonical, aclui/ISecurityInformation2::IsDaclCanonical, security.isecurityinformation2_isdaclcanonical
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
 - ISecurityInformation2::IsDaclCanonical
 - aclui/ISecurityInformation2::IsDaclCanonical
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
 - ISecurityInformation2.IsDaclCanonical
---

# ISecurityInformation2::IsDaclCanonical


## -description

The <b>IsDaclCanonical</b> method determines whether the ACEs contained in the specified DACL structure are ordered according to the definition of DACL ordering implemented by the client.

## -parameters

### -param pDacl [in]

A pointer to a discretionary 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure initialized by 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a>.

## -returns

Returns <b>TRUE</b> if the ACEs contained in the specified DACL structure are ordered according to the definition of DACL ordering implemented by the client.

Returns <b>FALSE</b> if the ACEs are not ordered correctly.

## -remarks

If the return value of this method is <b>FALSE</b>, the access control editor  displays a message box stating that the DACL is incorrectly ordered. If this method is not provided and the editor requires this information, the editor will check the  canonical ordering defined in 
<a href="/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl">Order of ACEs in a DACL</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation2">ISecurityInformation2</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a>