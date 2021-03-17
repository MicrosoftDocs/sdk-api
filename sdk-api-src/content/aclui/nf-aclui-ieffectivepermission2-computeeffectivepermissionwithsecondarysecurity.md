---
UID: NF:aclui.IEffectivePermission2.ComputeEffectivePermissionWithSecondarySecurity
title: IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity (aclui.h)
description: Computes the effective permissions by using the secondary security for an object.
helpviewer_keywords: ["ComputeEffectivePermissionWithSecondarySecurity","ComputeEffectivePermissionWithSecondarySecurity method [Security]","ComputeEffectivePermissionWithSecondarySecurity method [Security]","IEffectivePermission2 interface","IEffectivePermission2 interface [Security]","ComputeEffectivePermissionWithSecondarySecurity method","IEffectivePermission2.ComputeEffectivePermissionWithSecondarySecurity","IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity","aclui/IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity","security.ieffectivepermission2_computeeffectivepermissionwithsecondarysecurity"]
old-location: security\ieffectivepermission2_computeeffectivepermissionwithsecondarysecurity.htm
tech.root: security
ms.assetid: 03B73103-D7C0-4BA2-B315-3CC0049B1B8E
ms.date: 12/05/2018
ms.keywords: ComputeEffectivePermissionWithSecondarySecurity, ComputeEffectivePermissionWithSecondarySecurity method [Security], ComputeEffectivePermissionWithSecondarySecurity method [Security],IEffectivePermission2 interface, IEffectivePermission2 interface [Security],ComputeEffectivePermissionWithSecondarySecurity method, IEffectivePermission2.ComputeEffectivePermissionWithSecondarySecurity, IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity, aclui/IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity, security.ieffectivepermission2_computeeffectivepermissionwithsecondarysecurity
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
 - IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity
 - aclui/IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity
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
 - IEffectivePermission2.ComputeEffectivePermissionWithSecondarySecurity
---

# IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity


## -description

The <b>ComputeEffectivePermissionWithSecondarySecurity</b> method computes the effective permissions for an object. It supports integrating secondary or custom security policies. You may choose to provide this additional security information by implementing the <a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation4">ISecurityInformation4</a> interface. This method supports compound identity, which is when a principal's access token contains user and device authorization information.

## -parameters

### -param pSid [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that represents the security principal whose effective permission is being determined.

### -param pDeviceSid [in, optional]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that represents the device from which the principal is accessing the object. If this is not <b>NULL</b> and you are using the <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> function to compute the effective permissions, then the device SID may be compounded with the <i>pSid</i> parameter by using the <a href="/windows/desktop/api/authz/nf-authz-authzinitializecompoundcontext">AuthzInitializeCompoundContext</a> function.

### -param pszServerName [in, optional]

The name of the server on which the object resides. This is the same name that was returned from the <a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getobjectinformation">ISecurityInformation::GetObjectInformation</a> method.

### -param pSecurityObjects [in]

An array of security objects. This array is composed of objects that were deduced by the access control editor in addition to the ones returned from the <a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation4-getsecondarysecurity">ISecurityInformation4::GetSecondarySecurity</a> method.

### -param dwSecurityObjectCount [in]

The number of security objects in the <i>pSecurityObjects</i> parameter, and the number of results lists in the <i>pEffpermResultLists</i> parameter.

### -param pUserGroups [in, optional]

A pointer to additional user groups that should be used to modify the security context which was initialized from the <i>pSid</i> parameter.  If you are using the <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> function to compute the effective permissions, then the modification may be done by calling the <a href="/windows/desktop/api/authz/nf-authz-authzmodifysids">AuthzModifySids</a> function using         AuthzContextInfoGroupsSids as the  <i>SidClass</i> parameter.

### -param pAuthzUserGroupsOperations [in, optional]

Pointer to an array of <a href="/windows/desktop/api/authz/ne-authz-authz_sid_operation">AUTHZ_SID_OPERATION</a> structures that specify how the user groups in the authz context must be modified for each user group in the <i>pUserGroups</i> argument. This array contains as many elements as the number of groups in the <i>pUserGroups</i> parameter.

### -param pDeviceGroups [in, optional]

A pointer to additional device groups that should be used to modify the security context which was initialized from the <i>pSid</i> parameter or one that was created by compounding the contexts that were initialized from the <i>pSid</i> and <i>pDeviceSid</i> parameters.  If you are using the <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> function to compute the effective permissions, then the modification may be done by calling the <a href="/windows/desktop/api/authz/nf-authz-authzmodifysids">AuthzModifySids</a> function using         AuthzContextInfoDeviceSids as the  <i>SidClass</i> parameter.

### -param pAuthzDeviceGroupsOperations [in, optional]

Pointer to an array of <a href="/windows/desktop/api/authz/ne-authz-authz_sid_operation">AUTHZ_SID_OPERATION</a> enumeration types that specify how the device groups in the authz context must be modified for each device group in the <i>pDeviceGroups</i> argument. This array contains as many elements as the number of groups in the <i>pDeviceGroups</i> parameter.

### -param pAuthzUserClaims [in, optional]

Pointer to an <a href="/windows/desktop/api/authz/ns-authz-authz_security_attributes_information">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains  the user claims context that should be used to modify the security context that was initialized from the <i>pSid</i> parameter.  If you are using the <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> function to compute the effective permissions, then the modification may be done by calling the <a href="/windows/desktop/api/authz/nf-authz-authzmodifyclaims">AuthzModifyClaims</a> function using         AuthzContextInfoUserClaims as the  <i>ClaimClass</i> parameter.

### -param pAuthzUserClaimsOperations [in, optional]

Pointer to an <a href="/windows/desktop/api/authz/ne-authz-authz_security_attribute_operation">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a> enumeration type that specifies  the operations associated with the user claims context.

### -param pAuthzDeviceClaims [in, optional]

A pointer to the device claims context that should be used to modify the security context that was initialized from the <i>pSid</i> parameter or one that was created by compounding the contexts that were initialized from the <i>pSid</i> and <i>pDeviceSid</i> parameters.  This may be supplied by the caller, even if  the <i>pDeviceSid</i> parameter is not. If you are using the <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> function to compute the effective permissions, then the modification may be done by calling the <a href="/windows/desktop/api/authz/nf-authz-authzmodifyclaims">AuthzModifyClaims</a> function using         AuthzContextInfoDeviceClaims as the  <i>ClaimClass</i> parameter.

### -param pAuthzDeviceClaimsOperations [in, optional]

Pointer to an <a href="/windows/desktop/api/authz/ne-authz-authz_security_attribute_operation">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a> enumeration type that specifies the operations associated with the device claims context.

### -param pEffpermResultLists [in, out]

A pointer to an array of the effective permissions results of type <a href="/windows/desktop/api/aclui/ns-aclui-effperm_result_list">EFFPERM_RESULT_LIST</a>. This array is <i>dwSecurityObjectCount</i> elements long. The array is initialized by the caller and the implementation is expected to set all fields of each member in the array, indicating what access was granted by the corresponding security object.

If a security object was considered, the <b>fEvaluated</b> member should be set to <b>TRUE</b>.  In this case, the  <b>pObjectTypeList</b> and <b>pGrantedAccessList</b> members should both be <b>cObjectTypeListLength</b> elements long.  The <b>pObjectTypeList</b> member must point to memory that is owned by the resource manager and must remain valid until the <a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a> function exits.  The <b>pGrantedAccessList</b> member is freed by the caller by using the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.  If the resource manager does not support object ACEs, then the <b>pObjectTypeList</b> member should point to the <b>NULL</b> GUID, the <b>cObjectTypeListLength</b> member should be 1, and the <b>pGrantedAccessList</b> member should be a single <b>DWORD.</b>

## -returns

If the function is successful, the return value is S_OK.

If the function is successful but returned an approximate result, the return value is S_FALSE.

If the function fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

When the <b>Id</b> member the <a href="/windows/desktop/api/aclui/ns-aclui-security_object">SECURITY_OBJECT</a> structure is set to SECURITY_OBJECT_ID_CENTRAL_ACCESS_RULE, the <b>ComputeEffectivePermissionWithSecondarySecurity</b> method should use the <b>pData2</b> member first and only then evaluate access  by using the  <b>pData</b> member.

It is expected that the caller will use <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> to determine the effective permissions.  When possible, the implementation should initialize a remote resource manager on the supplied <b>pszServerName</b> member, using the <a href="/windows/desktop/api/authz/nf-authz-authzinitializeremoteresourcemanager">AuthzInitializeRemoteResourceManager</a> function to ensure that the groups and claims are initialized in the same manner as when the principal really accesses the object.  If <b>AuthzInitializeRemoteResourceManager</b> fails, the implementation may fall back to using the  <a href="/windows/desktop/api/authz/nf-authz-authzinitializeresourcemanager">AuthzInitializeResourceManager</a> function and return S_FALSE to indicate that approximate results are returned.

For each of the secondary security objects whose <b>fEvaluated</b> member is set to <b>TRUE</b>, the access control editor will display which permissions and properties were limited by that object using the <b>pwszName</b> member.

## -see-also

<a href="/windows/desktop/api/authz/ne-authz-authz_security_attribute_operation">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a>



<a href="/windows/desktop/api/authz/nf-authz-authzinitializeremoteresourcemanager">AuthzInitializeRemoteResourceManager</a>



<a href="/windows/desktop/api/aclui/nn-aclui-ieffectivepermission2">IEffectivePermission2</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation4-getsecondarysecurity">ISecurityInformation4::GetSecondarySecurity</a>



<a href="/windows/desktop/api/aclui/ns-aclui-security_object">SECURITY_OBJECT</a>