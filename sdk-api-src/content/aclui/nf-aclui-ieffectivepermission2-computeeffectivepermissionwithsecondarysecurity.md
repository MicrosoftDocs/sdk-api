---
UID: NF:aclui.IEffectivePermission2.ComputeEffectivePermissionWithSecondarySecurity
title: IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity
author: windows-sdk-content
description: Computes the effective permissions by using the secondary security for an object.
old-location: security\ieffectivepermission2_computeeffectivepermissionwithsecondarysecurity.htm
tech.root: SecAuthZ
ms.assetid: 03B73103-D7C0-4BA2-B315-3CC0049B1B8E
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ComputeEffectivePermissionWithSecondarySecurity, ComputeEffectivePermissionWithSecondarySecurity method [Security], ComputeEffectivePermissionWithSecondarySecurity method [Security],IEffectivePermission2 interface, IEffectivePermission2 interface [Security],ComputeEffectivePermissionWithSecondarySecurity method, IEffectivePermission2.ComputeEffectivePermissionWithSecondarySecurity, IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity, aclui/IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity, security.ieffectivepermission2_computeeffectivepermissionwithsecondarysecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - IEffectivePermission2.ComputeEffectivePermissionWithSecondarySecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEffectivePermission2::ComputeEffectivePermissionWithSecondarySecurity


## -description


The <b>ComputeEffectivePermissionWithSecondarySecurity</b> method computes the effective permissions for an object. It supports integrating secondary or custom security policies. You may choose to provide this additional security information by implementing the <a href="https://msdn.microsoft.com/F7AD3612-5D66-49DB-81EF-040849D32CB4">ISecurityInformation4</a> interface. This method supports compound identity, which is when a principal's access token contains user and device authorization information.


## -parameters




### -param pSid [in]

A pointer to a <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that represents the security principal whose effective permission is being determined.


### -param pDeviceSid [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that represents the device from which the principal is accessing the object. If this is not <b>NULL</b> and you are using the <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> function to compute the effective permissions, then the device SID may be compounded with the <i>pSid</i> parameter by using the <a href="https://msdn.microsoft.com/2EC9EE76-9A92-40DF-9884-547D96FF3E09">AuthzInitializeCompoundContext</a> function.


### -param pszServerName [in, optional]

The name of the server on which the object resides. This is the same name that was returned from the <a href="https://msdn.microsoft.com/2bc63aa0-dada-4962-a381-6b0f8332e564">ISecurityInformation::GetObjectInformation</a> method.


### -param pSecurityObjects [in]

An array of security objects. This array is composed of objects that were deduced by the access control editor in addition to the ones returned from the <a href="https://msdn.microsoft.com/20BD7D3B-1097-45CF-8237-0FBAD6BD6E3E">ISecurityInformation4::GetSecondarySecurity</a> method.


### -param dwSecurityObjectCount [in]

The number of security objects in the <i>pSecurityObjects</i> parameter, and the number of results lists in the <i>pEffpermResultLists</i> parameter.


### -param pUserGroups [in, optional]

A pointer to additional user groups that should be used to modify the security context which was initialized from the <i>pSid</i> parameter.  If you are using the <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> function to compute the effective permissions, then the modification may be done by calling the <a href="https://msdn.microsoft.com/740569A5-6159-409B-B8CB-B3A8BAE4F398">AuthzModifySids</a> function using         AuthzContextInfoGroupsSids as the  <i>SidClass</i> parameter.


### -param pAuthzUserGroupsOperations [in, optional]

Pointer to an array of <a href="https://msdn.microsoft.com/C312BE7D-DA1B-47FE-80BA-7506B9A26E9E">AUTHZ_SID_OPERATION</a> structures that specify how the user groups in the authz context must be modified for each user group in the <i>pUserGroups</i> argument. This array contains as many elements as the number of groups in the <i>pUserGroups</i> parameter.


### -param pDeviceGroups [in, optional]

A pointer to additional device groups that should be used to modify the security context which was initialized from the <i>pSid</i> parameter or one that was created by compounding the contexts that were initialized from the <i>pSid</i> and <i>pDeviceSid</i> parameters.  If you are using the <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> function to compute the effective permissions, then the modification may be done by calling the <a href="https://msdn.microsoft.com/740569A5-6159-409B-B8CB-B3A8BAE4F398">AuthzModifySids</a> function using         AuthzContextInfoDeviceSids as the  <i>SidClass</i> parameter.


### -param pAuthzDeviceGroupsOperations [in, optional]

Pointer to an array of <a href="https://msdn.microsoft.com/C312BE7D-DA1B-47FE-80BA-7506B9A26E9E">AUTHZ_SID_OPERATION</a> enumeration types that specify how the device groups in the authz context must be modified for each device group in the <i>pDeviceGroups</i> argument. This array contains as many elements as the number of groups in the <i>pDeviceGroups</i> parameter.


### -param pAuthzUserClaims [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a> structure that contains  the user claims context that should be used to modify the security context that was initialized from the <i>pSid</i> parameter.  If you are using the <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> function to compute the effective permissions, then the modification may be done by calling the <a href="https://msdn.microsoft.com/A93CD1DD-4E87-4C6A-928A-F90AD7F1085E">AuthzModifyClaims</a> function using         AuthzContextInfoUserClaims as the  <i>ClaimClass</i> parameter.


### -param pAuthzUserClaimsOperations [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/c1716cdb-87f9-47d6-bfc3-ae6cc043e917">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a> enumeration type that specifies  the operations associated with the user claims context.


### -param pAuthzDeviceClaims [in, optional]

A pointer to the device claims context that should be used to modify the security context that was initialized from the <i>pSid</i> parameter or one that was created by compounding the contexts that were initialized from the <i>pSid</i> and <i>pDeviceSid</i> parameters.  This may be supplied by the caller, even if  the <i>pDeviceSid</i> parameter is not. If you are using the <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> function to compute the effective permissions, then the modification may be done by calling the <a href="https://msdn.microsoft.com/A93CD1DD-4E87-4C6A-928A-F90AD7F1085E">AuthzModifyClaims</a> function using         AuthzContextInfoDeviceClaims as the  <i>ClaimClass</i> parameter.


### -param pAuthzDeviceClaimsOperations [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/c1716cdb-87f9-47d6-bfc3-ae6cc043e917">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a> enumeration type that specifies the operations associated with the device claims context.


### -param pEffpermResultLists [in, out]

A pointer to an array of the effective permissions results of type <a href="https://msdn.microsoft.com/D83C5632-F67A-42BA-A146-989EBB3B2763">EFFPERM_RESULT_LIST</a>. This array is <i>dwSecurityObjectCount</i> elements long. The array is initialized by the caller and the implementation is expected to set all fields of each member in the array, indicating what access was granted by the corresponding security object.

If a security object was considered, the <b>fEvaluated</b> member should be set to <b>TRUE</b>.  In this case, the  <b>pObjectTypeList</b> and <b>pGrantedAccessList</b> members should both be <b>cObjectTypeListLength</b> elements long.  The <b>pObjectTypeList</b> member must point to memory that is owned by the resource manager and must remain valid until the <a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a> function exits.  The <b>pGrantedAccessList</b> member is freed by the caller by using the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.  If the resource manager does not support object ACEs, then the <b>pObjectTypeList</b> member should point to the <b>NULL</b> GUID, the <b>cObjectTypeListLength</b> member should be 1, and the <b>pGrantedAccessList</b> member should be a single <b>DWORD.</b>


## -returns



If the function is successful, the return value is S_OK.

If the function is successful but returned an approximate result, the return value is S_FALSE.

If the function fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



When the <b>Id</b> member the <a href="https://msdn.microsoft.com/C3E61527-76AB-49E9-8BBD-486F437CC677">SECURITY_OBJECT</a> structure is set to SECURITY_OBJECT_ID_CENTRAL_ACCESS_RULE, the <b>ComputeEffectivePermissionWithSecondarySecurity</b> method should use the <b>pData2</b> member first and only then evaluate access  by using the  <b>pData</b> member.

It is expected that the caller will use <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> to determine the effective permissions.  When possible, the implementation should initialize a remote resource manager on the supplied <b>pszServerName</b> member, using the <a href="https://msdn.microsoft.com/C3B6C75B-13A5-49CC-BB01-DA1EEC292C20">AuthzInitializeRemoteResourceManager</a> function to ensure that the groups and claims are initialized in the same manner as when the principal really accesses the object.  If <b>AuthzInitializeRemoteResourceManager</b> fails, the implementation may fall back to using the  <a href="https://msdn.microsoft.com/e3f6b37d-2c33-4b17-97b4-762bf55561c5">AuthzInitializeResourceManager</a> function and return S_FALSE to indicate that approximate results are returned.

For each of the secondary security objects whose <b>fEvaluated</b> member is set to <b>TRUE</b>, the access control editor will display which permissions and properties were limited by that object using the <b>pwszName</b> member.




## -see-also




<a href="https://msdn.microsoft.com/c1716cdb-87f9-47d6-bfc3-ae6cc043e917">AUTHZ_SECURITY_ATTRIBUTE_OPERATION</a>



<a href="https://msdn.microsoft.com/C3B6C75B-13A5-49CC-BB01-DA1EEC292C20">AuthzInitializeRemoteResourceManager</a>



<a href="https://msdn.microsoft.com/2FDCA205-6880-4526-B8D7-6F9B107B218B">IEffectivePermission2</a>



<a href="https://msdn.microsoft.com/20BD7D3B-1097-45CF-8237-0FBAD6BD6E3E">ISecurityInformation4::GetSecondarySecurity</a>



<a href="https://msdn.microsoft.com/C3E61527-76AB-49E9-8BBD-486F437CC677">SECURITY_OBJECT</a>
 

 

