---
UID: NN:activationregistration.IExeServerActivatableClassRegistration
title: IExeServerActivatableClassRegistration
author: windows-sdk-content
description: Enables getting the registration info for an out-of-process server.
old-location: winrt\iexeserveractivatableclassregistration.htm
old-project: WinRT
ms.assetid: 1D8F7B12-2883-478D-B83D-84AC47D512E4
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: IExeServerActivatableClassRegistration, IExeServerActivatableClassRegistration interface [Windows Runtime], IExeServerActivatableClassRegistration interface [Windows Runtime],described, activationregistration/IExeServerActivatableClassRegistration, winrt.iexeserveractivatableclassregistration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: activationregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: ThreadingType
topic_type:
-	APIRef
-	kbSyntax
 - apiref
: 
api_type:
-	COM
 - HeaderDef
: 
api_location:
-	activationregistration.h
 - accctrl.h
: 
api_name:
-	IExeServerActivatableClassRegistration
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
 - InstancingType
: 
 - RegistrationScope
: 
 - ThreadingType
: 
 - IActivatableClassRegistration
: 
 - IDllServerActivatableClassRegistration
: 
 - IExeServerActivatableClassRegistration
: 
---

# IExeServerActivatableClassRegistration interface


## -description


Enables getting  the registration info for an out-of-process server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExeServerActivatableClassRegistration</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IExeServerActivatableClassRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExeServerActivatableClassRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6116DC84-2DE0-427E-BDC7-425178B08C1A">ServerRegistration</a>
</td>
<td align="left" width="63%">
Gets the registration details for an out-of-process server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/99834A2D-547B-4B04-8703-46B11E0BB812">IActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/00E9476E-45E0-4D97-9DA4-FD293674BED4">IDllServerActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/9A96968D-B9BD-4C47-B626-69B6EA6AE7EA">IExeServerRegistration</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>
 

 

