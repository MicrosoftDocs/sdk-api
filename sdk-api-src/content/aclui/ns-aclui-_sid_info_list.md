---
UID: NS:aclui._SID_INFO_LIST
title: "_SID_INFO_LIST"
author: windows-sdk-content
description: Contains a list of SID_INFO structures.
old-location: security\sid_info_list.htm
old-project: SecAuthZ
ms.assetid: e9be644c-ec56-4a49-9aa8-6b3f62d6cf0d
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PSID_INFO_LIST, PSID_INFO_LIST, PSID_INFO_LIST structure pointer [Security], SID_INFO_LIST, SID_INFO_LIST structure [Security], _SID_INFO_LIST, _win32_sid_info_list_str, aclui/PSID_INFO_LIST, aclui/SID_INFO_LIST, security.sid_info_list"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SID_INFO_LIST, *PSID_INFO_LIST
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
-	SID_INFO_LIST
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
 - _SECURITY_OBJECT
: 
 - _SID_INFO
: 
 - _SID_INFO_LIST
: 
---

# _SID_INFO_LIST structure


## -description


The <b>SID_INFO_LIST</b> structure contains a list of 
<a href="https://msdn.microsoft.com/6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c">SID_INFO</a> structures.


## -struct-fields




### -field cItems

The number of 
<a href="https://msdn.microsoft.com/6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c">SID_INFO</a> structures contained in the <b>aSidInfo</b> member.


### -field aSidInfo

A pointer to a list of <a href="https://msdn.microsoft.com/6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c">SID_INFO</a> structures that is returned by the 
<a href="https://msdn.microsoft.com/9a4056c6-6a21-4051-b4a6-c77351fce983">ISecurityInformation2::LookupSids</a> method.


## -see-also




<a href="https://msdn.microsoft.com/9a4056c6-6a21-4051-b4a6-c77351fce983">ISecurityInformation2::LookupSids</a>



<a href="https://msdn.microsoft.com/6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c">SID_INFO</a>
 

 

