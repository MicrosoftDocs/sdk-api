---
UID: NE:aclui._SI_PAGE_TYPE
title: SI_PAGE_TYPE (aclui.h)
description: Contains values that indicate the types of property pages in an access control editor property sheet.
helpviewer_keywords: ["SI_PAGE_ADVPERM","SI_PAGE_AUDIT","SI_PAGE_EFFECTIVE","SI_PAGE_OWNER","SI_PAGE_PERM","SI_PAGE_TAKEOWNERSHIP","SI_PAGE_TYPE","SI_PAGE_TYPE enumeration [Security]","_win32_si_page_type_str","aclui/SI_PAGE_ADVPERM","aclui/SI_PAGE_AUDIT","aclui/SI_PAGE_EFFECTIVE","aclui/SI_PAGE_OWNER","aclui/SI_PAGE_PERM","aclui/SI_PAGE_TAKEOWNERSHIP","aclui/SI_PAGE_TYPE","security.si_page_type"]
old-location: security\si_page_type.htm
tech.root: security
ms.assetid: 122b2dcb-5557-4692-a0d6-4a0accf71740
ms.date: 12/05/2018
ms.keywords: SI_PAGE_ADVPERM, SI_PAGE_AUDIT, SI_PAGE_EFFECTIVE, SI_PAGE_OWNER, SI_PAGE_PERM, SI_PAGE_TAKEOWNERSHIP, SI_PAGE_TYPE, SI_PAGE_TYPE enumeration [Security], _win32_si_page_type_str, aclui/SI_PAGE_ADVPERM, aclui/SI_PAGE_AUDIT, aclui/SI_PAGE_EFFECTIVE, aclui/SI_PAGE_OWNER, aclui/SI_PAGE_PERM, aclui/SI_PAGE_TAKEOWNERSHIP, aclui/SI_PAGE_TYPE, security.si_page_type
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SI_PAGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SI_PAGE_TYPE
 - aclui/_SI_PAGE_TYPE
 - SI_PAGE_TYPE
 - aclui/SI_PAGE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Aclui.h
api_name:
 - SI_PAGE_TYPE
---

# SI_PAGE_TYPE enumeration


## -description

The <b>SI_PAGE_TYPE</b> enumeration contains values that indicate the types of property pages in an access control editor property sheet.

## -enum-fields

### -field SI_PAGE_PERM

The 
<a href="/windows/desktop/SecAuthZ/basic-security-property-page">basic security property page</a> for editing the object's DACL.

### -field SI_PAGE_ADVPERM

The 
<a href="/windows/desktop/SecAuthZ/permissions-property-page">Permissions</a> tab for advanced editing of the object's DACL, such as editing object-specific ACEs.

### -field SI_PAGE_AUDIT

The 
<a href="/windows/desktop/SecAuthZ/auditing-property-page">Auditing</a> tab for editing the object's SACL.

### -field SI_PAGE_OWNER

The 
<a href="/windows/desktop/SecAuthZ/owner-property-page">Owner</a> tab for editing the object's owner.

### -field SI_PAGE_EFFECTIVE

The <b>Effective Permission</b> tab that displays the effective permissions granted to a specified user or group for access to the object.

### -field SI_PAGE_TAKEOWNERSHIP

A dialog box for changing the owner of the object.

### -field SI_PAGE_SHARE

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-propertysheetpagecallback">ISecurityInformation::PropertySheetPageCallback</a>