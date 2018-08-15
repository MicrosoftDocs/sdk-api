---
UID: NE:aclui._SI_PAGE_TYPE
title: "_SI_PAGE_TYPE"
author: windows-sdk-content
description: Contains values that indicate the types of property pages in an access control editor property sheet.
old-location: security\si_page_type.htm
old-project: secauthz
ms.assetid: 122b2dcb-5557-4692-a0d6-4a0accf71740
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SI_PAGE_ADVPERM, SI_PAGE_AUDIT, SI_PAGE_EFFECTIVE, SI_PAGE_OWNER, SI_PAGE_PERM, SI_PAGE_TAKEOWNERSHIP, SI_PAGE_TYPE, SI_PAGE_TYPE enumeration [Security], _SI_PAGE_TYPE, _win32_si_page_type_str, aclui/SI_PAGE_ADVPERM, aclui/SI_PAGE_AUDIT, aclui/SI_PAGE_EFFECTIVE, aclui/SI_PAGE_OWNER, aclui/SI_PAGE_PERM, aclui/SI_PAGE_TAKEOWNERSHIP, aclui/SI_PAGE_TYPE, security.si_page_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: aclui.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TreeSetNamedSecurityInfoW (Unicode) and TreeSetNamedSecurityInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SI_PAGE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Aclui.h
api_name:
 - SI_PAGE_TYPE
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# _SI_PAGE_TYPE enumeration


## -description


The <b>SI_PAGE_TYPE</b> enumeration contains values that indicate the types of property pages in an access control editor property sheet.


## -enum-fields




### -field SI_PAGE_PERM

The 
<a href="https://msdn.microsoft.com/6623fe7e-e91d-49c7-9ad0-7791c178d12b">basic security property page</a> for editing the object's DACL.


### -field SI_PAGE_ADVPERM

The 
<a href="https://msdn.microsoft.com/85a9fe30-871b-4909-b789-3fc257ffdbff">Permissions</a> tab for advanced editing of the object's DACL, such as editing object-specific ACEs.


### -field SI_PAGE_AUDIT

The 
<a href="https://msdn.microsoft.com/2a9152b7-c72d-4f03-bc3f-b75927fb4b6c">Auditing</a> tab for editing the object's SACL.


### -field SI_PAGE_OWNER

The 
<a href="https://msdn.microsoft.com/b0c421db-450e-4030-98e9-e062202e482c">Owner</a> tab for editing the object's owner.


### -field SI_PAGE_EFFECTIVE

The <b>Effective Permission</b> tab that displays the effective permissions granted to a specified user or group for access to the object.


### -field SI_PAGE_TAKEOWNERSHIP

A dialog box for changing the owner of the object.


### -field SI_PAGE_SHARE




## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/9b891e64-e648-44a4-add6-d4c214394be8">ISecurityInformation::PropertySheetPageCallback</a>
 

 

