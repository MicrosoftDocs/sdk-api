---
UID: NF:aclui.EditSecurity
title: EditSecurity function (aclui.h)
description: Displays a property sheet that contains a basic security property page. This property page enables the user to view and edit the access rights allowed or denied by the ACEs in an object's DACL.
helpviewer_keywords: ["EditSecurity","EditSecurity function [Security]","_win32_editsecurity","aclui/EditSecurity","security.editsecurity"]
old-location: security\editsecurity.htm
tech.root: security
ms.assetid: 756c94b0-946f-47eb-b4b4-db3e6e89fe46
ms.date: 12/05/2018
ms.keywords: EditSecurity, EditSecurity function [Security], _win32_editsecurity, aclui/EditSecurity, security.editsecurity
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
req.lib: Aclui.lib
req.dll: Aclui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EditSecurity
 - aclui/EditSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-aclui-l1-1-0.dll
 - Aclui.dll
api_name:
 - EditSecurity
---

# EditSecurity function


## -description

The <b>EditSecurity</b> function displays a property sheet that contains a 
<a href="/windows/desktop/SecAuthZ/basic-security-property-page">basic security property page</a>. This property page enables the user to view and edit the access rights allowed or denied by the ACEs in an object's DACL.

## -parameters

### -param hwndOwner [in]

A handle to the window that owns the property sheet. This parameter can be <b>NULL</b>.

### -param psi [in]

A pointer to your implementation of the 
<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a> interface. The system calls the interface methods to retrieve information about the object being edited and to return the user's input.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>EditSecurity</b> function calls the 
<a href="/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a> function to create a basic security property page.

During the property page initialization, the system calls the 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getsecurity">ISecurityInformation::GetSecurity</a> and 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-setsecurity">ISecurityInformation::SetSecurity</a> methods to determine whether the user has permission to edit the object's <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>. The system displays an error message if the user does not have permission.

The basic security property page can include an <b>Advanced</b> button for displaying the 
<a href="/windows/desktop/SecAuthZ/advanced-security-property-sheet">advanced security property sheet</a>. This advanced security property sheet can contain three additional property pages that enable the user to view and edit the object's DACL, SACL, and owner.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getsecurity">GetSecurity</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-setsecurity">SetSecurity</a>