---
UID: NF:aclui.EditSecurityAdvanced
title: EditSecurityAdvanced function (aclui.h)
description: Extends the EditSecurity function to include the security page type when displaying the property sheet that contains a basic security property page.
helpviewer_keywords: ["EditSecurityAdvanced","EditSecurityAdvanced function [Security]","aclui/EditSecurityAdvanced","security.editsecurityadvanced"]
old-location: security\editsecurityadvanced.htm
tech.root: security
ms.assetid: E451BBB9-4E01-4A8F-9ACD-750351F16453
ms.date: 12/05/2018
ms.keywords: EditSecurityAdvanced, EditSecurityAdvanced function [Security], aclui/EditSecurityAdvanced, security.editsecurityadvanced
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
req.lib: Aclui.lib
req.dll: Aclui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EditSecurityAdvanced
 - aclui/EditSecurityAdvanced
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
 - EditSecurityAdvanced
---

# EditSecurityAdvanced function


## -description

The <b>EditSecurityAdvanced</b> function extends the <a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a> function to include the security page type when displaying the property sheet that contains a 
<a href="/windows/desktop/SecAuthZ/basic-security-property-page">basic security property page</a>. This property page enables the user to view and edit the access rights allowed or denied by the <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) in an object's <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL).

## -parameters

### -param hwndOwner [in]

A handle to the window that owns the property sheet. This parameter can be <b>NULL</b>.

### -param psi [in]

A pointer to your implementation of the 
<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a> interface. The system calls the interface methods to retrieve information about the object being edited and to return the user's input.

### -param uSIPage [in]

A value of the 
<a href="/windows/desktop/api/aclui/ne-aclui-si_page_type">SI_PAGE_TYPE</a> enumeration that indicates the page type on which to display the elevated access control editor.

## -returns

If the function succeeds, the return value is S_OK.

If the function fails, any other <b>HRESULT</b> value indicates an error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a>



<a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getsecurity">GetSecurity</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-setsecurity">SetSecurity</a>