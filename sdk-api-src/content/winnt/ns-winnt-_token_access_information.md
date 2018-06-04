---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _TOKEN_ACCESS_INFORMATION structure


## -description


The <b>TOKEN_ACCESS_INFORMATION</b> structure specifies all the information in a token that is necessary to perform an access check.<div class="alert"><b>Note</b>  This structure doesn't contain token claim information. Applications that support conditional expression <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) should not use this structure for verifying access. For information about access validation support for conditional expressions, see the <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> and <a href="https://msdn.microsoft.com/c2d144f4-9eeb-4723-9d28-97cfd1a07274">AccessCheckAndAuditAlarm</a> functions.</div>
<div> </div>



## -struct-fields




### -field SidHash

A pointer to a <a href="https://msdn.microsoft.com/ef6e32f5-b47e-463e-a447-bed149b8d616">SID_AND_ATTRIBUTES_HASH</a> structure that specifies a hash of the token's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).


### -field RestrictedSidHash

A pointer to a <a href="https://msdn.microsoft.com/ef6e32f5-b47e-463e-a447-bed149b8d616">SID_AND_ATTRIBUTES_HASH</a> structure that specifies a hash of the token's restricted SID.


### -field Privileges

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556846">TOKEN_PRIVILEGES</a> structure that specifies information about the token's privileges.


### -field AuthenticationId

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structure that specifies the token's identity.


### -field TokenType

A value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556851">TOKEN_TYPE</a> enumeration that specifies the token's type.


### -field ImpersonationLevel

A value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556631">SECURITY_IMPERSONATION_LEVEL</a> enumeration that specifies the token's impersonation level.


### -field MandatoryPolicy

A <a href="https://msdn.microsoft.com/f5fc438b-c4f0-46f6-a188-52ce660d13da">TOKEN_MANDATORY_POLICY</a> structure that specifies the token's mandatory integrity policy.


### -field Flags

Reserved. Must be set to zero.


### -field AppContainerNumber

The app container number for the token or zero if this is not an app container token.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This member is not available.


### -field PackageSid

The app container SID or <b>NULL</b> if this is not an app container token.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This member is not available.


### -field CapabilitiesHash

Pointer to a <a href="https://msdn.microsoft.com/ef6e32f5-b47e-463e-a447-bed149b8d616">SID_AND_ATTRIBUTES_HASH</a> structure that specifies a hash of the token's capability SIDs.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This member is not available.


### -field TrustLevelSid

The protected process trust level of the token.


### -field SecurityAttributes

Reserved. Must be set to <b>NULL</b>.

<b>Prior to Windows 10:  </b>This member is not available.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556838">TOKEN_INFORMATION_CLASS</a>
 

 

