---
UID: NF:aclui.ISecurityInformation.PropertySheetPageCallback
title: ISecurityInformation::PropertySheetPageCallback (aclui.h)
description: The PropertySheetPageCallback method notifies an EditSecurity or CreateSecurityPage caller that an access control editor property page is being created or destroyed.
helpviewer_keywords: ["ISecurityInformation interface [Security]","PropertySheetPageCallback method","ISecurityInformation.PropertySheetPageCallback","ISecurityInformation::PropertySheetPageCallback","PSPCB_CREATE","PSPCB_RELEASE","PSPCB_SI_INITDIALOG","PropertySheetPageCallback","PropertySheetPageCallback method [Security]","PropertySheetPageCallback method [Security]","ISecurityInformation interface","_win32_isecurityinformation_propertysheetpagecallback","aclui/ISecurityInformation::PropertySheetPageCallback","security.isecurityinformation_propertysheetpagecallback"]
old-location: security\isecurityinformation_propertysheetpagecallback.htm
tech.root: security
ms.assetid: 9b891e64-e648-44a4-add6-d4c214394be8
ms.date: 12/05/2018
ms.keywords: ISecurityInformation interface [Security],PropertySheetPageCallback method, ISecurityInformation.PropertySheetPageCallback, ISecurityInformation::PropertySheetPageCallback, PSPCB_CREATE, PSPCB_RELEASE, PSPCB_SI_INITDIALOG, PropertySheetPageCallback, PropertySheetPageCallback method [Security], PropertySheetPageCallback method [Security],ISecurityInformation interface, _win32_isecurityinformation_propertysheetpagecallback, aclui/ISecurityInformation::PropertySheetPageCallback, security.isecurityinformation_propertysheetpagecallback
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISecurityInformation::PropertySheetPageCallback
 - aclui/ISecurityInformation::PropertySheetPageCallback
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
 - ISecurityInformation.PropertySheetPageCallback
---

# ISecurityInformation::PropertySheetPageCallback


## -description

The <b>PropertySheetPageCallback</b> method notifies an 
<a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a> or 
<a href="/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a> caller that an access control editor property page is being created or destroyed.

## -parameters

### -param hwnd [in]

If <i>uMsg</i> is PSPCB_SI_INITDIALOG, <i>hwnd</i> is a handle to the property page dialog box. Otherwise, <i>hwnd</i> is <b>NULL</b>.

### -param uMsg [in]

Identifies the message being received. This parameter is one of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PSPCB_CREATE"></a><a id="pspcb_create"></a><dl>
<dt><b>PSPCB_CREATE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a property page is being created.

</td>
</tr>
<tr>
<td width="40%"><a id="PSPCB_RELEASE"></a><a id="pspcb_release"></a><dl>
<dt><b>PSPCB_RELEASE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a property page is being destroyed.

</td>
</tr>
<tr>
<td width="40%"><a id="PSPCB_SI_INITDIALOG"></a><a id="pspcb_si_initdialog"></a><dl>
<dt><b>PSPCB_SI_INITDIALOG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a property page is being initialized.

</td>
</tr>
</table>

### -param uPage [in]

A value from the 
<a href="/windows/desktop/api/aclui/ne-aclui-si_page_type">SI_PAGE_TYPE</a> enumeration type that indicates the type of access control editor property page being created or destroyed.

## -returns

Returns S_OK if successful.

Returns a nonzero error code if an error occurs.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a>



<a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/api/aclui/ne-aclui-si_page_type">SI_PAGE_TYPE</a>