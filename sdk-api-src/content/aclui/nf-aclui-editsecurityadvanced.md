---
UID: NF:aclui.EditSecurityAdvanced
title: EditSecurityAdvanced function
author: windows-sdk-content
description: Extends the EditSecurity function to include the security page type when displaying the property sheet that contains a basic security property page.
old-location: security\editsecurityadvanced.htm
old-project: SecAuthZ
ms.assetid: E451BBB9-4E01-4A8F-9ACD-750351F16453
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: EditSecurityAdvanced, EditSecurityAdvanced function [Security], aclui/EditSecurityAdvanced, security.editsecurityadvanced
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclui.h
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
tech.root: 
req.typenames: SI_PAGE_TYPE
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
-	Aclui.dll
 - accctrl.h
: 
api_name:
-	EditSecurityAdvanced
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
req.lib: Aclui.lib
req.dll: Aclui.dll
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
---

# EditSecurityAdvanced function


## -description


The <b>EditSecurityAdvanced</b> function extends the <a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a> function to include the security page type when displaying the property sheet that contains a 
<a href="https://msdn.microsoft.com/6623fe7e-e91d-49c7-9ad0-7791c178d12b">basic security property page</a>. This property page enables the user to view and edit the access rights allowed or denied by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) in an object's <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL).


## -parameters




### -param hwndOwner [in]

A handle to the window that owns the property sheet. This parameter can be <b>NULL</b>.


### -param psi [in]

A pointer to your implementation of the 
<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a> interface. The system calls the interface methods to retrieve information about the object being edited and to return the user's input.


### -param uSIPage [in]

A value of the 
<a href="https://msdn.microsoft.com/122b2dcb-5557-4692-a0d6-4a0accf71740">SI_PAGE_TYPE</a> enumeration that indicates the page type on which to display the elevated access control editor.


## -returns



If the function succeeds, the return value is S_OK.

If the function fails, any other <b>HRESULT</b> value indicates an error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="authorization_functions.htm">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/52cb20fd-7f3a-4984-a898-f4b9e9738e1a">CreateSecurityPage</a>



<a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a>



<a href="https://msdn.microsoft.com/4c9e05fd-0b58-4d6d-b33e-067d9e8e2915">GetSecurity</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>



<a href="https://msdn.microsoft.com/7c23c5ad-8088-4cfb-9746-99d24cc3bd0e">SetSecurity</a>
 

 

