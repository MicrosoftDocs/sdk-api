---
UID: NF:certenroll.IX509Enrollment.CreatePFX
title: IX509Enrollment::CreatePFX
author: windows-sdk-content
description: Creates a Personal Information Exchange (PFX) message.
old-location: security\ix509enrollment_createpfx_method.htm
old-project: seccertenroll
ms.assetid: 4a51bea0-e7f8-4a4e-b612-95616b126466
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreatePFX, CreatePFX method [Security], CreatePFX method [Security],IX509Enrollment interface, IX509Enrollment interface [Security],CreatePFX method, IX509Enrollment.CreatePFX, IX509Enrollment::CreatePFX, certenroll/IX509Enrollment::CreatePFX, security.ix509enrollment_createpfx_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509Enrollment.CreatePFX
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509Enrollment::CreatePFX


## -description


The <b>CreatePFX</b> method creates a Personal Information Exchange (PFX) message. The message is contained in a byte array that is encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) standard.  The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.


## -parameters




### -param strPassword [in]

A <b>BSTR</b> variable that contains a password for the PFX message. This can be  <b>NULL</b> to indicate that  no password is used.  When you have finished using the password, clear it from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information about protecting the password, see <a href="https://msdn.microsoft.com/en-us/library/ms717799(v=VS.85).aspx">Handling Passwords</a>.


### -param ExportOptions [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa379073(v=VS.85).aspx">PFXExportOptions</a> enumeration value that specifies how much of the certificate chain is exported. You can export the certificate only, the certificate chain without the root, or the entire chain.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the DER-encoded  message. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.


### -param pValue [out]

Pointer to a <b>BSTR</b> variable that contains the DER-encoded PFX message.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
No  certificate chain can be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>OLE_E_BLANK</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The enrollment object has not been initialized.

</td>
</tr>
</table>
 




## -remarks



The PFX format is also known as PKCS #12. The <b>CreatePFX</b> method:<ul>
<li>Opens the certificate store in memory for the default provider.</li>
<li>Adds the installed certificate to the store or builds the certificate chain adds a link to it.</li>
<li>Exports the certificate and the private key to a PFX message depending on the export options specified.</li>
<li>Encodes the exported message by using DER.</li>
</ul>


Before calling this method, you must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> object by calling one of the following methods.<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378046(v=VS.85).aspx">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377872(v=VS.85).aspx">InitializeFromRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378023(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>Further, you must return successfully from the <a href="https://msdn.microsoft.com/en-us/library/Aa377871(v=VS.85).aspx">Enroll</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a>
 

 

