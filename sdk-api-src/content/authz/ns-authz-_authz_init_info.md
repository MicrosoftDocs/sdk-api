---
UID: NS:authz._AUTHZ_INIT_INFO
title: "_AUTHZ_INIT_INFO"
author: windows-sdk-content
description: Defines the initialization information for the resource manager.
old-location: security\authz_init_info.htm
old-project: secauthz
ms.assetid: 30489BE7-5B95-413E-8134-039AD3220A50
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: "*PAUTHZ_INIT_INFO, AUTHZ_INIT_INFO, AUTHZ_INIT_INFO structure [Security], PAUTHZ_INIT_INFO, PAUTHZ_INIT_INFO structure pointer [Security], _AUTHZ_INIT_INFO, authz/AUTHZ_INIT_INFO, authz/PAUTHZ_INIT_INFO, security.authz_init_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: authz.h
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
tech.root: 
req.typenames: AUTHZ_INIT_INFO, *PAUTHZ_INIT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_INIT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _AUTHZ_INIT_INFO structure


## -description


The <b>AUTHZ_INIT_INFO</b> structure defines the initialization information for the resource manager.


## -struct-fields




### -field version

The version of the authorization resource manager initialization information structure. This must be set to AUTHZ_INIT_INFO_VERSION_V1 (1).


### -field szResourceManagerName

Pointer to a Unicode string that identifies the resource manager. This parameter can be <b>NULL</b> if the resource manager does not need a name.


### -field pfnDynamicAccessCheck

Pointer to an <a href="https://msdn.microsoft.com/e8a510e6-0739-4765-ad07-3bcb1b9c905c">AuthzAccessCheckCallback</a> callback function that the resource manager calls each time it encounters a callback access control entry (ACE) during access control list (ACL) evaluation in <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> or <a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a>. This parameter can be <b>NULL</b> if no access check callback function is used. 



### -field pfnComputeDynamicGroups

Pointer to the <a href="https://msdn.microsoft.com/c20a02a0-5303-4433-a484-5a89999b32b9">AuthzComputeGroupsCallback</a> callback function called by the resource manager during initialization of an AuthzClientContext handle. This parameter can be <b>NULL</b> if no callback function is used to compute dynamic groups.


### -field pfnFreeDynamicGroups

Pointer to the <a href="https://msdn.microsoft.com/5563311c-2bd1-4e96-ba0a-5a4225050f77">AuthzFreeGroupsCallback</a> callback function called by the resource manager to free security identifier (SID) attribute arrays allocated by the compute dynamic groups callback. This parameter can be <b>NULL</b> if no callback function is used to compute dynamic groups.


### -field pfnGetCentralAccessPolicy

Pointer to the <a href="https://msdn.microsoft.com/1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0">AuthzGetCentralAccessPolicyCallback</a> callback function to be called by the resource manager to resolve any Central Access Policy ID ACE (<a href="https://msdn.microsoft.com/library/windows/hardware/hh406640">SYSTEM_SCOPED_POLICY_ID_ACE</a>) encountered by <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> or <a href="https://msdn.microsoft.com/8b3bb69f-7bf9-4e4a-b870-081dd92c7ee4">AuthzCachedAccessCheck</a>. If this parameter is <b>NULL</b>, the <b>AuthzAccessCheck</b> function will fall back to LSA to resolve the Central Access Policy ID ACE.


### -field pfnFreeCentralAccessPolicy

Pointer to the <a href="https://msdn.microsoft.com/F0859A67-4D20-4189-8F35-A78034E41E6A">AuthzFreeCentralAccessPolicyCallback</a> callback function called by the resource manager to free the Central Access Policy allocated by the callback to get a central access policy. This parameter can be <b>NULL</b> if no callback function is specified for pfnGetCentralAccessPolicy

