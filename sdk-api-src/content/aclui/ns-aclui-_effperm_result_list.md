---
UID: NS:aclui._EFFPERM_RESULT_LIST
title: "_EFFPERM_RESULT_LIST"
author: windows-sdk-content
description: Lists the effective permissions.
old-location: security\effperm_result_list.htm
old-project: SecAuthZ
ms.assetid: D83C5632-F67A-42BA-A146-989EBB3B2763
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PEFFPERM_RESULT_LIST, EFFPERM_RESULT_LIST, EFFPERM_RESULT_LIST structure [Security], PEFFPERM_RESULT_LIST, PEFFPERM_RESULT_LIST structure pointer [Security], _EFFPERM_RESULT_LIST, aclui/EFFPERM_RESULT_LIST, aclui/PEFFPERM_RESULT_LIST, security.effperm_result_list"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: EFFPERM_RESULT_LIST, *PEFFPERM_RESULT_LIST
topic_type:
-	APIRef
-	kbSyntax
 - apiref
: 
api_type:
-	HeaderDef
 - HeaderDef
: 
api_location:
-	Aclui.h
 - accctrl.h
: 
api_name:
-	EFFPERM_RESULT_LIST
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
req.lib: 
req.dll: 
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
 - GetTrusteeFormW
: 
 - GetTrusteeNameA
: 
 - GetTrusteeNameW
: 
 - GetTrusteeTypeA
: 
 - GetTrusteeTypeW
: 
 - LookupSecurityDescriptorPartsA
: 
 - LookupSecurityDescriptorPartsW
: 
 - SetEntriesInAclA
: 
 - SetEntriesInAclW
: 
 - SetNamedSecurityInfoA
: 
 - SetNamedSecurityInfoW
: 
 - SetSecurityInfo
: 
 - TreeResetNamedSecurityInfoA
: 
 - TreeResetNamedSecurityInfoW
: 
 - TreeSetNamedSecurityInfoA
: 
 - TreeSetNamedSecurityInfoW
: 
 - aclui.h
: 
 - _SI_PAGE_TYPE
: 
 - CreateSecurityPage
: 
 - EditSecurity
: 
 - EditSecurityAdvanced
: 
 - _EFFPERM_RESULT_LIST
: 
---

# _EFFPERM_RESULT_LIST structure


## -description


The <b>EFFPERM_RESULT_LIST</b> structure lists the effective permissions.


## -struct-fields




### -field fEvaluated

Indicates if the effective permissions results have been evaluated.


### -field cObjectTypeListLength

The number of elements in both the <b>pObjectTypeList</b> and <b>pGrantedAccessList</b> members.


### -field pObjectTypeList

A pointer to an array of <a href="https://msdn.microsoft.com/c729ff1a-65f3-4f6f-84dd-5700aead75ce">OBJECT_TYPE_LIST</a> structures that specifies the properties and property sets for which access was evaluated.


### -field pGrantedAccessList

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> values that specifies the access rights granted for each corresponding object type.

