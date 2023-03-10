---
UID: NF:aclui.CreateSecurityPage
title: CreateSecurityPage function (aclui.h)
description: Creates a basic security property page that enables the user to view and edit the access rights allowed or denied by the access control entries (ACEs) in an object's discretionary access control list (DACL).
helpviewer_keywords: ["CreateSecurityPage","CreateSecurityPage function [Security]","_win32_createsecuritypage","aclui/CreateSecurityPage","security.createsecuritypage"]
old-location: security\createsecuritypage.htm
tech.root: security
ms.assetid: 52cb20fd-7f3a-4984-a898-f4b9e9738e1a
ms.date: 12/05/2018
ms.keywords: CreateSecurityPage, CreateSecurityPage function [Security], _win32_createsecuritypage, aclui/CreateSecurityPage, security.createsecuritypage
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
 - CreateSecurityPage
 - aclui/CreateSecurityPage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Aclui.dll
api_name:
 - CreateSecurityPage
---

# CreateSecurityPage function


## -description

The <b>CreateSecurityPage</b> function creates a 
<a href="/windows/desktop/SecAuthZ/basic-security-property-page">basic security property page</a> that enables the user to view and edit the access rights allowed or denied by the <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) in an object's <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL). Use the 
<a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function or the 
<a href="/windows/desktop/Controls/psm-addpage">PSM_ADDPAGE</a> message to add this page to a property sheet.

## -parameters

### -param psi [in]

A pointer to your implementation of the 
<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a> interface. The system calls the interface methods to retrieve information about the object being edited and to return the user's input.

## -returns

If the function succeeds, the function returns a handle to a basic security property page.
						

If the function fails, it returns <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

During the property page initialization, the system calls the 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getsecurity">ISecurityInformation::GetSecurity</a> and 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-setsecurity">ISecurityInformation::SetSecurity</a> methods to determine whether the user has permission to edit the object's <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>. The system displays an error message if the user does not have permission.

The basic security property page can include an <b>Advanced</b> button for displaying the 
<a href="/windows/desktop/SecAuthZ/advanced-security-property-sheet">advanced security property sheet</a>. This advanced security property sheet can contain three additional property pages that enable the user to view and edit the object's DACL, <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL), and owner.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getsecurity">GetSecurity</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/Controls/psm-addpage">PSM_ADDPAGE</a>



<a href="/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-setsecurity">SetSecurity</a>