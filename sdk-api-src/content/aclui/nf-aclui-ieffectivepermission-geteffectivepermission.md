---
UID: NF:aclui.IEffectivePermission.GetEffectivePermission
title: IEffectivePermission::GetEffectivePermission (aclui.h)
description: Returns the effective permission for an object type.
helpviewer_keywords: ["GetEffectivePermission","GetEffectivePermission method [Security]","GetEffectivePermission method [Security]","IEffectivePermission interface","IEffectivePermission interface [Security]","GetEffectivePermission method","IEffectivePermission.GetEffectivePermission","IEffectivePermission::GetEffectivePermission","aclui/IEffectivePermission::GetEffectivePermission","security.ieffectivepermission_geteffectivepermission"]
old-location: security\ieffectivepermission_geteffectivepermission.htm
tech.root: security
ms.assetid: fef2dfe0-3c56-4502-9e8d-900aea84318b
ms.date: 12/05/2018
ms.keywords: GetEffectivePermission, GetEffectivePermission method [Security], GetEffectivePermission method [Security],IEffectivePermission interface, IEffectivePermission interface [Security],GetEffectivePermission method, IEffectivePermission.GetEffectivePermission, IEffectivePermission::GetEffectivePermission, aclui/IEffectivePermission::GetEffectivePermission, security.ieffectivepermission_geteffectivepermission
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
 - IEffectivePermission::GetEffectivePermission
 - aclui/IEffectivePermission::GetEffectivePermission
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
 - IEffectivePermission.GetEffectivePermission
---

# IEffectivePermission::GetEffectivePermission


## -description

The <b>GetEffectivePermission</b> method returns the effective permission for an object type.

## -parameters

### -param pguidObjectType [in]

A <b>GUID</b> for the object type whose permission is being queried.

### -param pUserSid [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that represents the security principal whose effective permission is being determined.

### -param pszServerName [in]

A pointer to null-terminated wide character string that represents the server name.

### -param pSD [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that represents the object's  <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>. The security descriptor is used to perform the access check.

### -param ppObjectTypeList [out]

A pointer to a pointer to an <a href="/windows/desktop/api/winnt/ns-winnt-object_type_list">OBJECT_TYPE_LIST</a> structure that represents the array of object types in the object tree for the object. If an object does not support property access, use the following technique to specify the value for the <b>OBJECT_TYPE_LIST</b>.


```cpp
#include <windows.h>

OBJECT_TYPE_LIST g_DefaultOTL[] = {
 {0, 0, (LPGUID)&GUID_NULL},
};


```

### -param pcObjectTypeListLength [out]

A pointer to a <b>ULONG</b> that receives the count of object types pointed to by  <i>ppObjectTypeList</i>.

### -param ppGrantedAccessList [out]

A pointer to a pointer to an <a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> that receives the array of granted access masks. The operating system will use <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to free the memory allocated for this parameter.

### -param pcGrantedAccessListLength [out]

A pointer to a <b>ULONG</b> variable that receives the count of granted access masks pointed to by  the <i>ppGrantedAccessList</i> parameter.

## -returns

If the function is successful, the return value is S_OK.

If the function fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.