---
UID: NF:aclui.ISecurityInformation3.OpenElevatedEditor
title: ISecurityInformation3::OpenElevatedEditor (aclui.h)
description: Opens an access control editor when a user clicks the Edit button on an access control editor page that displays an image of a shield on that Edit button.
helpviewer_keywords: ["ISecurityInformation3 interface [Security]","OpenElevatedEditor method","ISecurityInformation3.OpenElevatedEditor","ISecurityInformation3::OpenElevatedEditor","OpenElevatedEditor","OpenElevatedEditor method [Security]","OpenElevatedEditor method [Security]","ISecurityInformation3 interface","aclui/ISecurityInformation3::OpenElevatedEditor","security.isecurityinformation3_openelevatededitor"]
old-location: security\isecurityinformation3_openelevatededitor.htm
tech.root: security
ms.assetid: 4ed50e6b-4c4a-48bf-ad7c-133064a4be47
ms.date: 12/05/2018
ms.keywords: ISecurityInformation3 interface [Security],OpenElevatedEditor method, ISecurityInformation3.OpenElevatedEditor, ISecurityInformation3::OpenElevatedEditor, OpenElevatedEditor, OpenElevatedEditor method [Security], OpenElevatedEditor method [Security],ISecurityInformation3 interface, aclui/ISecurityInformation3::OpenElevatedEditor, security.isecurityinformation3_openelevatededitor
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISecurityInformation3::OpenElevatedEditor
 - aclui/ISecurityInformation3::OpenElevatedEditor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation3.OpenElevatedEditor
---

# ISecurityInformation3::OpenElevatedEditor


## -description

The <b>OpenElevatedEditor</b> method opens an access control editor when a user clicks the <b>Edit</b> button on an access control editor page that displays an image of a shield on that <b>Edit</b> button. The image of a shield is displayed when the access control editor is launched by a process with a token that lacks permission to save changes to the object being edited.

## -parameters

### -param hWnd [in]

The parent window of the access control editor.

### -param uPage [in]

A value of the <a href="/windows/desktop/api/aclui/ne-aclui-si_page_type">SI_PAGE_TYPE</a> enumeration that indicates the page type on which to display the elevated access control editor.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation3-getfullresourcename">GetFullResourceName</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation3">ISecurityInformation3</a>