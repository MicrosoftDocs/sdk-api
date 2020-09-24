---
UID: NF:aclui.ISecurityInformation.GetObjectInformation
title: ISecurityInformation::GetObjectInformation (aclui.h)
description: The GetObjectInformation method requests information that the access control editor uses to initialize its pages and to determine the editing options available to the user.
helpviewer_keywords: ["GetObjectInformation","GetObjectInformation method [Security]","GetObjectInformation method [Security]","ISecurityInformation interface","ISecurityInformation interface [Security]","GetObjectInformation method","ISecurityInformation.GetObjectInformation","ISecurityInformation::GetObjectInformation","_win32_isecurityinformation_getobjectinformation","aclui/ISecurityInformation::GetObjectInformation","security.isecurityinformation_getobjectinformation"]
old-location: security\isecurityinformation_getobjectinformation.htm
tech.root: security
ms.assetid: 2bc63aa0-dada-4962-a381-6b0f8332e564
ms.date: 12/05/2018
ms.keywords: GetObjectInformation, GetObjectInformation method [Security], GetObjectInformation method [Security],ISecurityInformation interface, ISecurityInformation interface [Security],GetObjectInformation method, ISecurityInformation.GetObjectInformation, ISecurityInformation::GetObjectInformation, _win32_isecurityinformation_getobjectinformation, aclui/ISecurityInformation::GetObjectInformation, security.isecurityinformation_getobjectinformation
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
 - ISecurityInformation::GetObjectInformation
 - aclui/ISecurityInformation::GetObjectInformation
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
 - ISecurityInformation.GetObjectInformation
---

# ISecurityInformation::GetObjectInformation


## -description

The <b>GetObjectInformation</b> method requests information that the access control editor uses to initialize its pages and to determine the editing options available to the user.

## -parameters

### -param pObjectInfo [out]

A pointer to an 
<a href="/windows/desktop/api/aclui/ns-aclui-si_object_info">SI_OBJECT_INFO</a> structure. Your implementation must fill this structure to pass information back to the access control editor.

## -returns

Returns S_OK if successful.

Returns a nonzero error code if an error occurs.

## -remarks

The system does not free the string pointers that you return in the 
<a href="/windows/desktop/api/aclui/ns-aclui-si_object_info">SI_OBJECT_INFO</a> structure.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/api/aclui/ns-aclui-si_object_info">SI_OBJECT_INFO</a>