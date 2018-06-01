---
UID: NN:activation.IActivationFactory
title: IActivationFactory
author: windows-sdk-content
description: Enables classes to be activated by the Windows Runtime.
old-location: winrt\iactivationfactory.htm
old-project: WinRT
ms.assetid: C6A2ED6E-9C45-4CF3-A301-72A5DAEB4DFC
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: IActivationFactory, IActivationFactory interface [Windows Runtime], IActivationFactory interface [Windows Runtime],described, activation/IActivationFactory, winrt.iactivationfactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: activation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: SI_OBJECT_INFO, *PSI_OBJECT_INFO
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
-	Activation.h
 - accctrl.h
: 
api_name:
-	IActivationFactory
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
---

# IActivationFactory interface


## -description


Enables classes to be activated by the Windows Runtime.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActivationFactory</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IActivationFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActivationFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AE3E2D87-3AE7-42C3-AA1D-510E717D2E51">ActivateInstance</a>
</td>
<td align="left" width="63%">
Creates a new instance of the Windows Runtime class that is associated with the current activation factory.

</td>
</tr>
</table> 


## -remarks



Implement the <b>IActivationFactory</b> interface when you create a class that you want Windows Runtime  applications to use. Clients call the <a href="https://msdn.microsoft.com/AE3E2D87-3AE7-42C3-AA1D-510E717D2E51">ActivateInstance</a>
    method to use an instance of your class. 

You can get an <b>IActivationFactory</b> pointer by calling the <a href="https://msdn.microsoft.com/291ed35d-a459-4509-a265-89c49f8aa13a">RoGetActivationFactory</a> function.  

During activation of a class, the Windows Runtime calls the <a href="https://msdn.microsoft.com/59660F0E-C2BE-4670-86B7-8C9CBA025910">DllGetActivationFactory</a> function to get an <b>IActivationFactory</b> pointer that corresponds to the requested class. 




## -see-also




<a href="https://msdn.microsoft.com/59660F0E-C2BE-4670-86B7-8C9CBA025910">DllGetActivationFactory</a>



<a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>



<a href="https://msdn.microsoft.com/291ed35d-a459-4509-a265-89c49f8aa13a">RoGetActivationFactory</a>
 

 

