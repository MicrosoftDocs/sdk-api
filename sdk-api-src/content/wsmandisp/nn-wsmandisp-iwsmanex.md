---
UID: NN:wsmandisp.IWSManEx
title: IWSManEx (wsmandisp.h)
description: Extends the methods and properties of the IWSMan interface to include creating IWSManResourceLocator objects, methods that return enumeration and session flag values, and a method to get extended error information.
helpviewer_keywords: ["IWSManEx","IWSManEx interface [Windows Remote Management]","IWSManEx interface [Windows Remote Management]","described","winrm.iwsmanex","wsmandisp/ IWSManEx"]
old-location: winrm\iwsmanex.htm
tech.root: winrm
ms.assetid: 23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6
ms.date: 12/05/2018
ms.keywords: IWSManEx, IWSManEx interface [Windows Remote Management], IWSManEx interface [Windows Remote Management],described, winrm.iwsmanex, wsmandisp/ IWSManEx
f1_keywords:
- wsmandisp/IWSManEx
dev_langs:
- c++
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WSMAuto.dll
api_name:
- IWSManEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManEx interface


## -description


Extends the methods and properties of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsman">IWSMan</a> 
    interface to include creating 
    <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> objects, methods that return 
    enumeration and session flag values, and a method to get extended error information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n"> IWSManEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsman">IWSMan</a>. <b> IWSManEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b> IWSManEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">CreateResourceLocator</a>
</td>
<td align="left" width="63%">
Creates a new instance of an 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword">IWSManEx.SessionFlagCredUsernamePassword</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagCredUsernamePassword</b> for use 
     in the <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport">IWSManEx.SessionFlagEnableSPNServerPort</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagEnableSPNServerPort</b> for use 
     in the <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption">IWSManEx.SessionFlagNoEncryption</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagNoEncryption</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck">IWSManEx.SessionFlagSkipCACheck</a>
</td>
<td align="left" width="63%">
Returns the value of the  authentication flag <b>WSManFlagSkipCACheck</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck">IWSManEx.SessionFlagSkipCNCheck</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagSkipCNCheck</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagusebasic">IWSManEx.SessionFlagUseBasic</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseBasic</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman-createsession">IWSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagusedigest">IWSManEx.SessionFlagUseDigest</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseDigest</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman-createsession">WSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate">IWSManEx.SessionFlagUseNegotiate</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseNegotiate</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman-createsession">WSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication">IWSManEx.SessionFlagUseNoAuthentication</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseNoAuthentication</b> for use 
     in the <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman-createsession">WSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagutf8">IWSManEx.SessionFlagUTF8</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUTF8</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman-createsession">WSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos">IWSManEx.WSMan.SessionFlagUseKerberos</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseKerberos</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman-createsession">WSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep">IWSManEx::EnumerationFlagHierarchyDeep</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>EnumerationFlagHierarchyDeep</b> for use 
     in the <i>flags</i> parameter of the 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly">IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant 
     <b>EnumerationFlagHierarchyDeepBasePropsOnly</b> for use in the 
     <i>flags</i> parameter of the 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow">IWSManEx::EnumerationFlagHierarchyShallow</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>EnumerationFlagHierarchyShallow</b> for 
     use in the <i>flags</i> parameter of the 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext">IWSManEx::EnumerationFlagNonXmlText</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>WSManFlagNonXmlText</b> for use in the 
     <i>flags</i> parameter of the 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext">IWSManEx::EnumerationFlagNonXmlText</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>WSManFlagNonXmlText</b> for use in the 
     <i>flags</i> parameter of the 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr">IWSManEx::EnumerationFlagReturnEPR</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>EnumerationFlagReturnEPR</b> for use in 
     the <i>flags</i> parameter of the 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject">IWSManEx::EnumerationFlagReturnObject</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>EnumerationFlagReturnObject</b> for use 
     in the <i>flags</i> parameter of the 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr">IWSManEx::EnumerationFlagReturnObjectAndEPR</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>EnumerationFlagReturnObjectAndEPR</b> 
     for use in the <i>flags</i> parameter of the 
     <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanex-geterrormessage">IWSManEx::GetErrorMessage</a>
</td>
<td align="left" width="63%">
Returns a formatted string containing the text of an error number.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsman">IWSMan</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman">WSMan</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>
 

 

