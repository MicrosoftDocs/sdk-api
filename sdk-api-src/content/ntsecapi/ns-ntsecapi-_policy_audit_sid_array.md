---
UID: NS:ntsecapi._POLICY_AUDIT_SID_ARRAY
title: "_POLICY_AUDIT_SID_ARRAY"
author: windows-sdk-content
description: Specifies an array of SID structures that represent Windows users or groups.
old-location: security\policy_audit_sid_array.htm
old-project: SecAuthZ
ms.assetid: 22f4255c-331a-4327-84d8-e905c7e419b6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PPOLICY_AUDIT_SID_ARRAY, POLICY_AUDIT_SID_ARRAY, POLICY_AUDIT_SID_ARRAY structure [Security], PPOLICY_AUDIT_SID_ARRAY, PPOLICY_AUDIT_SID_ARRAY structure pointer [Security], _POLICY_AUDIT_SID_ARRAY, ntsecapi/POLICY_AUDIT_SID_ARRAY, ntsecapi/PPOLICY_AUDIT_SID_ARRAY, security.policy_audit_sid_array"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: POLICY_AUDIT_SID_ARRAY, *PPOLICY_AUDIT_SID_ARRAY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	POLICY_AUDIT_SID_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _POLICY_AUDIT_SID_ARRAY structure


## -description


The <b>POLICY_AUDIT_SID_ARRAY</b> structure specifies an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structures that represent Windows users or groups.


## -struct-fields




### -field UsersCount

The number of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structures in the <b>UserSidArray</b> array.


### -field UserSidArray.size_is

 


### -field UserSidArray.size_is.UsersCount

 


### -field UserSidArray

A pointer to an array of pointers to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structures that specify Windows users or groups.


## -see-also




<a href="https://msdn.microsoft.com/4b13f021-ba08-4eb8-9c7a-0512992ef272">AuditEnumeratePerUserPolicy</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

