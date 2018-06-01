---
UID: NE:activationregistration.IdentityType
title: IdentityType
author: windows-sdk-content
description: Represents the kind of activation for an out-of-process server.
old-location: winrt\identitytype.htm
old-project: WinRT
ms.assetid: 17EBFEE2-903A-4B64-A59F-D94E96E4457E
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: ActivateAsActivator, ActivateAsPackage, IdentityType, IdentityType enumeration [Windows Runtime], RunAs, activationregistration/ActivateAsActivator, activationregistration/ActivateAsPackage, activationregistration/IdentityType, activationregistration/RunAs, winrt.identitytype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: activationregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Activation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IdentityType
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
-	activationregistration.h
 - accctrl.h
: 
api_name:
-	IdentityType
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
 - _SI_ACCESS
: 
 - _SI_INHERIT_TYPE
: 
 - _SI_OBJECT_INFO
: 
 - COM
: 
 - activation.h
: 
 - IActivationFactory.ActivateInstance
: 
 - IActivationFactory
: 
 - activationregistration.h
: 
 - ActivationType
: 
 - IdentityType
: 
---

# IdentityType enumeration


## -description


Represents the kind of activation for an out-of-process server.


## -enum-fields




### -field IdentityType_ActivateAsActivator


### -field IdentityType_RunAs


### -field IdentityType_ActivateAsPackage


### -field IdentityType_SessionVirtual


### -field IdentityType_SessionUser


### -field IdentityType_ActivateAsActivatingUser


### -field int




#### - ActivateAsActivator

Activate the out-of-process server as an activator.


#### - ActivateAsPackage

Activate the out-of-process server as a Windows Store app package.


#### - RunAs

Activate the out-of-process server as an executable.


## -see-also




<a href="https://msdn.microsoft.com/1D8F7B12-2883-478D-B83D-84AC47D512E4">IExeServerActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/9A96968D-B9BD-4C47-B626-69B6EA6AE7EA">IExeServerRegistration</a>
 

 

