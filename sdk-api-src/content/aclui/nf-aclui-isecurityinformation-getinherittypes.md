---
UID: NF:aclui.ISecurityInformation.GetInheritTypes
title: ISecurityInformation::GetInheritTypes (aclui.h)
description: The GetInheritTypes method requests information about how ACEs can be inherited by child objects. For more information, see ACE Inheritance.
helpviewer_keywords: ["GetInheritTypes","GetInheritTypes method [Security]","GetInheritTypes method [Security]","ISecurityInformation interface","ISecurityInformation interface [Security]","GetInheritTypes method","ISecurityInformation.GetInheritTypes","ISecurityInformation::GetInheritTypes","_win32_isecurityinformation_getinherittypes","aclui/ISecurityInformation::GetInheritTypes","security.isecurityinformation_getinherittypes"]
old-location: security\isecurityinformation_getinherittypes.htm
tech.root: security
ms.assetid: dafe6c45-616f-4339-a119-9b88055b5d3a
ms.date: 12/05/2018
ms.keywords: GetInheritTypes, GetInheritTypes method [Security], GetInheritTypes method [Security],ISecurityInformation interface, ISecurityInformation interface [Security],GetInheritTypes method, ISecurityInformation.GetInheritTypes, ISecurityInformation::GetInheritTypes, _win32_isecurityinformation_getinherittypes, aclui/ISecurityInformation::GetInheritTypes, security.isecurityinformation_getinherittypes
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
 - ISecurityInformation::GetInheritTypes
 - aclui/ISecurityInformation::GetInheritTypes
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
 - ISecurityInformation.GetInheritTypes
---

# ISecurityInformation::GetInheritTypes


## -description

The <b>GetInheritTypes</b> method requests information about how ACEs can be inherited by child objects. For more information, see 
<a href="/windows/desktop/SecAuthZ/ace-inheritance">ACE Inheritance</a>.

## -parameters

### -param ppInheritTypes [out]

A pointer to a variable you should set to a pointer to an array of 
<a href="/windows/desktop/api/aclui/ns-aclui-si_inherit_type">SI_INHERIT_TYPE</a> structures. The array should include one entry for each combination of inheritance flags and child object type that you support.

### -param pcInheritTypes [out]

A pointer to a variable that you should set to indicate the number of entries in the <i>ppInheritTypes</i> array.

## -returns

Returns S_OK if successful.

Returns a nonzero error code if an error occurs.

## -remarks

The access control editor does not free the pointer returned in <i>ppInheritTypes</i>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a>



<a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/api/aclui/ns-aclui-si_inherit_type">SI_INHERIT_TYPE</a>