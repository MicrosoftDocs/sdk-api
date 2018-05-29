---
UID: NF:certenroll.IPolicyQualifier.InitializeEncode
title: IPolicyQualifier::InitializeEncode
author: windows-sdk-content
description: Initializes the object from a string and a value that identifies the qualifier type.
old-location: security\ipolicyqualifier_initializeencode_method.htm
old-project: SecCertEnroll
ms.assetid: fc8b5916-0557-4f9b-8478-169a3dd9cebc
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IPolicyQualifier interface [Security],InitializeEncode method, IPolicyQualifier.InitializeEncode, IPolicyQualifier::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IPolicyQualifier interface, PolicyQualifierTypeUnknown, PolicyQualifierTypeUrl, PolicyQualifierTypeUserNotice, certenroll/IPolicyQualifier::InitializeEncode, security.ipolicyqualifier_initializeencode_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IPolicyQualifier.InitializeEncode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IPolicyQualifier::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the object from a string and a value that identifies the qualifier type.


## -parameters




### -param strQualifier [in]

A <b>BSTR</b> variable that contains the qualifier.


### -param Type [in]

A <a href="https://msdn.microsoft.com/76cd1874-b80d-466e-9c7d-12cf8d310b8a">PolicyQualifierType</a> enumeration value that specifies the type of qualifier applied to a certificate policy. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PolicyQualifierTypeUnknown"></a><a id="policyqualifiertypeunknown"></a><a id="POLICYQUALIFIERTYPEUNKNOWN"></a><dl>
<dt><b><b>PolicyQualifierTypeUnknown</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The qualifier type is not specified.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyQualifierTypeUrl"></a><a id="policyqualifiertypeurl"></a><a id="POLICYQUALIFIERTYPEURL"></a><dl>
<dt><b><b>PolicyQualifierTypeUrl</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The qualifier is a URL that points to a Certification Practice Statement (CPS) that has been defined by the certification authority to outline the policies under which the certificate was issued and the purposes for which the certificate can be used.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyQualifierTypeUserNotice"></a><a id="policyqualifiertypeusernotice"></a><a id="POLICYQUALIFIERTYPEUSERNOTICE"></a><dl>
<dt><b><b>PolicyQualifierTypeUserNotice</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The qualifier is a text statement to be displayed by the application to any user who relies on the certificate. The user notice identifies the permitted uses of the certificate.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



If you specify <b>PolicyQualifierTypeUrl</b> in the <i>Type</i> parameter, this method associates the string entered in the <i>strQualifier</i> parameter with the <b>XCN_OID_PKIX_POLICY_QUALIFIER_CPS</b> (1.3.6.1.5.5.7.2.1) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and encodes it by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER). The URL is encoded as an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) IA5 string.

If you specify <b>PolicyQualifierTypeUserNotice</b> in the <i>Type</i> parameter, this method associates the string entered in the <i>strQualifier</i> parameter with the <b>XCN_OID_PKIX_POLICY_QUALIFIER_USERNOTICE</b> (1.3.6.1.5.5.7.2.2) OID and encodes it by using DER.

You can retrieve the following properties for this object:<ul>
<li>The <a href="https://msdn.microsoft.com/d19efcd3-c5fc-4268-af39-2385b7babcc9">ObjectId</a> property retrieves an OID that identifies whether the qualifier is a CPS or a user notice.</li>
<li>The <a href="https://msdn.microsoft.com/73cecc9b-519c-45c8-b9f8-864ff628560a">Qualifier</a> property retrieves the string specified for the <i>strQualifier</i> parameter of the <b>InitializeEncode</b> method.</li>
<li>The <a href="https://msdn.microsoft.com/a654f60c-7f67-4fe2-847b-e8c5f91fde80">RawData</a> property retrieves the DER-encoded qualifier.</li>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property retrieves a value of the <a href="https://msdn.microsoft.com/76cd1874-b80d-466e-9c7d-12cf8d310b8a">PolicyQualifierType</a> enumeration that specifies the qualifier type.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/3804e372-17bb-458d-8da5-85d760fe5e60">IPolicyQualifier</a>
 

 

