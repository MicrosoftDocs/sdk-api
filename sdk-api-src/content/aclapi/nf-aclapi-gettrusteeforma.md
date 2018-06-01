---
UID: NF:aclapi.GetTrusteeFormA
title: GetTrusteeFormA function
author: windows-sdk-content
description: Retrieves the trustee name from the specified TRUSTEE structure. This value indicates whether the structure uses a name string or a security identifier (SID) to identify the trustee.
old-location: security\gettrusteeform.htm
old-project: SecAuthZ
ms.assetid: e5e450b8-0b7b-4324-b453-5c020e74b1ee
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetTrusteeForm, GetTrusteeForm function [Security], GetTrusteeFormA, GetTrusteeFormW, _win32_gettrusteeform, aclapi/GetTrusteeForm, aclapi/GetTrusteeFormA, aclapi/GetTrusteeFormW, security.gettrusteeform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTrusteeFormW (Unicode) and GetTrusteeFormA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRUSTEE_W, *PTRUSTEE_W, TRUSTEEW, *PTRUSTEEW
topic_type:
-	APIRef
-	kbSyntax
 - apiref
: 
api_type:
-	DllExport
 - HeaderDef
: 
api_location:
-	Advapi32.dll
 - accctrl.h
: 
api_name:
-	GetTrusteeForm
-	GetTrusteeFormA
-	GetTrusteeFormW
 - _ACCESS_MODE
: 
product: Windows
targetos: Windows
 - _MULTIPLE_TRUSTEE_OPERATION
: 
 - _PROGRESS_INVOKE_SETTING
: 
 - _SE_OBJECT_TYPE
: 
 - _TRUSTEE_FORM
: 
 - _TRUSTEE_TYPE
: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
 - _ACTRL_ACCESS_ENTRYA
: 
 - _ACTRL_ACCESS_ENTRYW
: 
 - _ACTRL_ACCESS_ENTRY_LISTA
: 
 - _ACTRL_ACCESS_ENTRY_LISTW
: 
 - _ACTRL_ALISTA
: 
 - _ACTRL_ALISTW
: 
 - _ACTRL_PROPERTY_ENTRYA
: 
 - _ACTRL_PROPERTY_ENTRYW
: 
 - _EXPLICIT_ACCESS_A
: 
 - _EXPLICIT_ACCESS_W
: 
 - _INHERITED_FROMA
: 
 - _INHERITED_FROMW
: 
 - _OBJECTS_AND_NAME_A
: 
 - _OBJECTS_AND_NAME_W
: 
 - _OBJECTS_AND_SID
: 
 - _TRUSTEE_A
: 
 - _TRUSTEE_W
: 
req.irql: 
 - 
: 
 - BuildExplicitAccessWithNameA
: 
 - BuildExplicitAccessWithNameW
: 
 - BuildSecurityDescriptorA
: 
 - BuildSecurityDescriptorW
: 
 - BuildTrusteeWithNameA
: 
 - BuildTrusteeWithNameW
: 
 - BuildTrusteeWithObjectsAndNameA
: 
 - BuildTrusteeWithObjectsAndNameW
: 
 - BuildTrusteeWithObjectsAndSidA
: 
 - BuildTrusteeWithObjectsAndSidW
: 
 - BuildTrusteeWithSidA
: 
 - BuildTrusteeWithSidW
: 
 - FreeInheritedFromArray
: 
 - GetAuditedPermissionsFromAclA
: 
 - GetAuditedPermissionsFromAclW
: 
 - GetEffectiveRightsFromAclA
: 
 - GetEffectiveRightsFromAclW
: 
 - GetExplicitEntriesFromAclA
: 
 - GetExplicitEntriesFromAclW
: 
 - GetInheritanceSourceA
: 
 - GetInheritanceSourceW
: 
 - GetNamedSecurityInfoA
: 
 - GetNamedSecurityInfoW
: 
 - GetSecurityInfo
: 
 - GetTrusteeFormA
: 
---

# GetTrusteeFormA function


## -description


The <b>GetTrusteeForm</b> function retrieves the trustee name from the specified <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure. This value indicates whether the structure uses a name string or a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) to identify the trustee.


## -parameters




### -param pTrustee [in]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


## -returns




						The return value is one of the constants from the 
<a href="https://msdn.microsoft.com/991ac6cb-3fc9-4915-b5c9-ae73efb25d68">TRUSTEE_FORM</a> enumeration.
					




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/9d3ce528-fb28-4e2e-bf7f-7d84c697fcb6">GetTrusteeName</a>



<a href="https://msdn.microsoft.com/19777929-43cf-45ea-8283-e42bf9ce8d7a">GetTrusteeType</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>



<a href="https://msdn.microsoft.com/991ac6cb-3fc9-4915-b5c9-ae73efb25d68">TRUSTEE_FORM</a>
 

 

