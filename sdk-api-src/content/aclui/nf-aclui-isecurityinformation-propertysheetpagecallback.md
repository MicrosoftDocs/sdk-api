---
UID: NF:aclui.ISecurityInformation.PropertySheetPageCallback
title: ISecurityInformation::PropertySheetPageCallback
author: windows-sdk-content
description: The PropertySheetPageCallback method notifies an EditSecurity or CreateSecurityPage caller that an access control editor property page is being created or destroyed.
old-location: security\isecurityinformation_propertysheetpagecallback.htm
tech.root: secauthz
ms.assetid: 9b891e64-e648-44a4-add6-d4c214394be8
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ISecurityInformation interface [Security],PropertySheetPageCallback method, ISecurityInformation.PropertySheetPageCallback, ISecurityInformation::PropertySheetPageCallback, PSPCB_CREATE, PSPCB_RELEASE, PSPCB_SI_INITDIALOG, PropertySheetPageCallback, PropertySheetPageCallback method [Security], PropertySheetPageCallback method [Security],ISecurityInformation interface, _win32_isecurityinformation_propertysheetpagecallback, aclui/ISecurityInformation::PropertySheetPageCallback, security.isecurityinformation_propertysheetpagecallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation.PropertySheetPageCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityInformation::PropertySheetPageCallback


## -description


The <b>PropertySheetPageCallback</b> method notifies an 
<a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a> or 
<a href="https://msdn.microsoft.com/52cb20fd-7f3a-4984-a898-f4b9e9738e1a">CreateSecurityPage</a> caller that an access control editor property page is being created or destroyed.


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
<a href="https://msdn.microsoft.com/122b2dcb-5557-4692-a0d6-4a0accf71740">SI_PAGE_TYPE</a> enumeration type that indicates the type of access control editor property page being created or destroyed.


## -returns



Returns S_OK if successful.

Returns a nonzero error code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="authorization_functions.htm">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/52cb20fd-7f3a-4984-a898-f4b9e9738e1a">CreateSecurityPage</a>



<a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>



<a href="https://msdn.microsoft.com/122b2dcb-5557-4692-a0d6-4a0accf71740">SI_PAGE_TYPE</a>
 

 

