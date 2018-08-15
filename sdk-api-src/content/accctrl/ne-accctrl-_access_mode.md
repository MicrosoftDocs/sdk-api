---
UID: NE:accctrl._ACCESS_MODE
title: "_ACCESS_MODE"
author: windows-sdk-content
description: Contains values that indicate how the access rights in an EXPLICIT_ACCESS structure apply to the trustee.
old-location: security\access_mode.htm
old-project: secauthz
ms.assetid: 52d1b3a3-eed5-4603-9056-520320da2a52
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ACCESS_MODE, ACCESS_MODE enumeration [Security], DENY_ACCESS, GRANT_ACCESS, NOT_USED_ACCESS, REVOKE_ACCESS, SET_ACCESS, SET_AUDIT_FAILURE, SET_AUDIT_SUCCESS, _ACCESS_MODE, _win32_access_mode_str, accctrl/ACCESS_MODE, accctrl/DENY_ACCESS, accctrl/GRANT_ACCESS, accctrl/NOT_USED_ACCESS, accctrl/REVOKE_ACCESS, accctrl/SET_ACCESS, accctrl/SET_AUDIT_FAILURE, accctrl/SET_AUDIT_SUCCESS, security.access_mode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: accctrl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ACCESS_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - ACCESS_MODE
product: Windows
targetos: Windows
---

# _ACCESS_MODE enumeration


## -description


The <b>ACCESS_MODE</b> enumeration contains values that indicate how the access rights in an 
<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure apply to the trustee. Functions such as 
<a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a> and 
<a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a> use these values to set or retrieve information in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE).


## -enum-fields




### -field NOT_USED_ACCESS

Value not used.


### -field GRANT_ACCESS

Indicates an 
<a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a> structure. The new ACE combines the specified rights with any existing allowed or denied rights of the trustee.


### -field SET_ACCESS

Indicates an <a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a>structure that allows the specified rights. 




On input, this value discards any existing access control information for the trustee.


### -field DENY_ACCESS

Indicates an 
<a href="https://msdn.microsoft.com/d76a92d0-ccd0-4e73-98b6-43bcd661134d">ACCESS_DENIED_ACE</a>structure that denies the specified rights. 




On input, this value denies the specified rights in addition to any currently denied rights of the trustee.


### -field REVOKE_ACCESS

Indicates that all existing <a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a> or 
<a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a> structures for the specified trustee are removed.


### -field SET_AUDIT_SUCCESS

Indicates a <a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a>structure that generates audit messages for successful attempts to use the specified access rights. 
						

On input, this value combines the specified rights with any existing audited access rights for the trustee.


### -field SET_AUDIT_FAILURE

Indicates a 
<a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a>structure that generates audit messages for failed attempts to use the specified access rights.  

On input, this value combines the specified rights with any existing audited access rights for the trustee.


## -see-also




<a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a>



<a href="https://msdn.microsoft.com/d76a92d0-ccd0-4e73-98b6-43bcd661134d">ACCESS_DENIED_ACE</a>



<a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACE</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a>



<a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a>



<a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a>



<a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a>
 

 

