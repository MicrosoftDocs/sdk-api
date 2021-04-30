---
UID: NF:aclui.ISecurityInformation4.GetSecondarySecurity
title: ISecurityInformation4::GetSecondarySecurity (aclui.h)
description: Returns additional security contexts that may impact access to the resource.
helpviewer_keywords: ["GetSecondarySecurity","GetSecondarySecurity method [Security]","GetSecondarySecurity method [Security]","ISecurityInformation4 interface","ISecurityInformation4 interface [Security]","GetSecondarySecurity method","ISecurityInformation4.GetSecondarySecurity","ISecurityInformation4::GetSecondarySecurity","aclui/ISecurityInformation4::GetSecondarySecurity","security.isecurityinformation4_getsecondarysecurity"]
old-location: security\isecurityinformation4_getsecondarysecurity.htm
tech.root: security
ms.assetid: 20BD7D3B-1097-45CF-8237-0FBAD6BD6E3E
ms.date: 12/05/2018
ms.keywords: GetSecondarySecurity, GetSecondarySecurity method [Security], GetSecondarySecurity method [Security],ISecurityInformation4 interface, ISecurityInformation4 interface [Security],GetSecondarySecurity method, ISecurityInformation4.GetSecondarySecurity, ISecurityInformation4::GetSecondarySecurity, aclui/ISecurityInformation4::GetSecondarySecurity, security.isecurityinformation4_getsecondarysecurity
req.header: aclui.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ISecurityInformation4::GetSecondarySecurity
 - aclui/ISecurityInformation4::GetSecondarySecurity
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
 - ISecurityInformation4.GetSecondarySecurity
---

# ISecurityInformation4::GetSecondarySecurity


## -description

The <b>GetSecondarySecurity</b> method returns additional security contexts that may impact access to the resource.

## -parameters

### -param pSecurityObjects [out]

An array of <a href="/windows/desktop/api/aclui/ns-aclui-security_object">SECURITY_OBJECT</a> structures that contain the secondary security objects associated with the resources that are set on success. The array is owned by the caller and is freed by using the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function. The <b>pwszName</b> member is also freed by using <b>LocalFree</b>. If the <b>cbData</b> or <b>cbData2</b> members of the <b>SECURITY_OBJECT</b> structure are not zero, then the caller must free the corresponding <b>pData</b> or <b>pData2</b> by using <b>LocalFree</b>. If either of those members are zero, then the corresponding <b>pData</b> and <b>pData2</b> members are owned by the resource manager and must remain valid until the <a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a> function returns

### -param pSecurityObjectCount [out]

The number of security objects in the <i>pSecurityObjects</i> parameter that are set on success.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

A resource manager does not need to return secondary objects with the <b>fWellKnown</b> member set to <b>TRUE</b> and the <b>Id</b> member set to SECURITY_OBJECT_ID_OBJECT_SD, SECURITY_OBJECT_ID_CENTRAL_POLICY, or SECURITY_OBJECT_ID_CENTRAL_ACCESS_RULE. Security objects with these IDs will be provided by the access control editor when calling <a href="/windows/desktop/api/aclui/nf-aclui-ieffectivepermission2-computeeffectivepermissionwithsecondarysecurity">ComputeEffectivePermissionWithSecondarySecurity</a>.

Interpretation of the returned security objects is tied to the implementation of <a href="/windows/desktop/api/aclui/nf-aclui-ieffectivepermission2-computeeffectivepermissionwithsecondarysecurity">ComputeEffectivePermissionWithSecondarySecurity</a>.

## -see-also

<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation4">ISecurityInformation4</a>