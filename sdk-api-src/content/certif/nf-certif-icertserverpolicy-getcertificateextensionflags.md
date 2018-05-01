---
UID: NF:certif.ICertServerPolicy.GetCertificateExtensionFlags
title: ICertServerPolicy::GetCertificateExtensionFlags method
author: windows-driver-content
description: Retrieves the flags associated with the extension acquired by the most recent call to GetCertificateExtension.
old-location: security\icertserverpolicy_getcertificateextensionflags.htm
old-project: SecCrypto
ms.assetid: 6266e96d-81da-478f-99da-86936b4cfc6b
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: CCertServerPolicy object [Security], GetCertificateExtensionFlags method, GetCertificateExtensionFlags method [Security], GetCertificateExtensionFlags method [Security], CCertServerPolicy object, GetCertificateExtensionFlags method [Security], ICertServerPolicy interface, GetCertificateExtensionFlags,ICertServerPolicy.GetCertificateExtensionFlags, ICertServerPolicy, ICertServerPolicy interface [Security], GetCertificateExtensionFlags method, ICertServerPolicy::GetCertificateExtensionFlags, _certsrv_icertserverpolicy_getcertificateextensionflags, certif/ICertServerPolicy::GetCertificateExtensionFlags, security.icertserverpolicy_getcertificateextensionflags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certif.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certcli.dll
api_name:
-	ICertServerPolicy.GetCertificateExtensionFlags
-	CCertServerPolicy.GetCertificateExtensionFlags
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
---

# ICertServerPolicy::GetCertificateExtensionFlags method


## -description


The <b>GetCertificateExtensionFlags</b> method retrieves the  flags associated with the extension acquired by the most recent call to 
<a href="https://msdn.microsoft.com/e2c8e1d5-6ddb-4c8f-8052-f45cd52e2bef">GetCertificateExtension</a>.


## -parameters




### -param pExtFlags [out]

A pointer to a <b>LONG</b> variable that contains the extension flags.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pExtFlags</i> parameter contains the flags from the extension acquired by the most recent call to <a href="https://msdn.microsoft.com/e2c8e1d5-6ddb-4c8f-8052-f45cd52e2bef">GetCertificateExtension</a>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the flags from the extension acquired by the most recent call to <a href="https://msdn.microsoft.com/e2c8e1d5-6ddb-4c8f-8052-f45cd52e2bef">GetCertificateExtension</a>.




## -remarks



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff556644">SetContext</a> and <a href="https://msdn.microsoft.com/e2c8e1d5-6ddb-4c8f-8052-f45cd52e2bef">GetCertificateExtension</a> methods must be called before <b>GetCertificateExtensionFlags</b>. The <b>SetContext</b> method specifies which request is used as the current context, and the <b>GetCertificateExtension</b> method retrieves the extensions for the request.

Extensions can contain policy and origin flags. Policy flags provide information about the certificate extension. Policy flags can be set by the policy module. Origin flags indicate the module that set the certificate extension. Origin flags are only set by the server engine.

One or more policy flags can be returned from an extension. The following are predefined policy flags.<table>
<tr>
<th>Policy flag value</th>
<th>Explanation</th>
</tr>
<tr>
<td>EXTENSION_CRITICAL_FLAG</td>
<td>This is a critical extension.</td>
</tr>
<tr>
<td>EXTENSION_DISABLE_FLAG</td>
<td>Extension will not be used.</td>
</tr>
</table>
 



One of the following origin flags can also be returned.<table>
<tr>
<th>Origin flag value</th>
<th>Explanation</th>
</tr>
<tr>
<td>EXTENSION_ORIGIN_REQUEST</td>
<td>The extension was extracted from an array of extensions stored in the szOID_CERT_EXTENSIONS (1.3.6.1.4.1.311.2.1.14) or szOID_RSA_certExtensions (1.2.840.113549.1.9.14) attribute of a PKCS #10 request.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_POLICY</td>
<td>The policy module set the extension.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_ADMIN</td>
<td>The administrator set the extension. For more information, see 
<a href="https://msdn.microsoft.com/d26061da-acc3-45d8-93de-f2d431d350a6">ICertAdmin::SetCertificateExtension</a>.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_SERVER</td>
<td>The server engine set the extension.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_RENEWALCERT</td>
<td>The extension was extracted from the certificate stored in the szOID_RENEWAL_CERTIFICATE (1.3.6.1.4.1.311.13.1) attribute of a PKCS #10 renewal request.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_IMPORTEDCERT</td>
<td>The extension was extracted from an imported certificate (the certificate was passed to 
<a href="https://msdn.microsoft.com/b79a726e-5823-468b-869d-382e6fd73b44">ICertAdmin::ImportCertificate</a>).</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_PKCS7</td>
<td>The extension was extracted from an array of extensions stored in the szOID_CERT_EXTENSIONS (1.3.6.1.4.1.311.2.1.14) or szOID_RSA_certExtensions (1.2.840.113549.1.9.14) attribute of a PKCS #7 request.</td>
</tr>
</table>
 



Predefined masks are provided for ease of use in determining which flags are set in the return value. The following masks are provided.<table>
<tr>
<th>Mask value</th>
<th>Explanation</th>
</tr>
<tr>
<td>EXTENSION_POLICY_MASK</td>
<td>This value (0x0000FFFF) is used to examine policy flags.</td>
</tr>
<tr>
<td>EXTENSION_ORIGIN_MASK</td>
<td>This value (0x000F0000) is used to examine origin flags.</td>
</tr>
</table>
 



It is safe to use the high 8 bits of EXTENSION_POLICY_MASK for custom data. These bits will be saved persistently in the database, but will not be written to the certificate extensions.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT  hr;
LONG     ExtFlags;
// pCertServerPolicy has been used to call SetContext previously.
hr = pCertServerPolicy-&gt;GetCertificateExtensionFlags( &amp;ExtFlags);

// More than one policy flag might be set.
LONG ExtPolicyFlags = ExtFlags &amp; EXTENSION_POLICY_MASK;

if (ExtPolicyFlags &amp; EXTENSION_CRITICAL_FLAG)
{
    // Do something.
}

if (ExtPolicyFlags &amp; EXTENSION_DISABLE_FLAG)
{
    // Do something.
}

// only one origin flag can be set
switch (ExtFlags &amp; EXTENSION_ORIGIN_MASK)
{
    case EXTENSION_ORIGIN_REQUEST:
        // Extension was set in certificate request.
        break;
    case EXTENSION_ORIGIN_POLICY:
        // Extension was set by policy module.
        break;
    case EXTENSION_ORIGIN_ADMIN:
        // Extension was set by administrator.
        break;
    case EXTENSION_ORIGIN_SERVER:
        // Extension was set by server engine.
        break;
    default:
        break;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d26061da-acc3-45d8-93de-f2d431d350a6">ICertAdmin::SetCertificateExtension</a>



<a href="https://msdn.microsoft.com/7d16161e-9827-46a0-9989-30ebca792bb1">ICertServerPolicy</a>



<a href="https://msdn.microsoft.com/e2c8e1d5-6ddb-4c8f-8052-f45cd52e2bef">ICertServerPolicy::GetCertificateExtension</a>



<a href="https://msdn.microsoft.com/ba45cda8-49a5-4bd6-af68-90b4b56aff7d">ICertServerPolicy::SetContext</a>



<a href="https://msdn.microsoft.com/c175eba9-ea7c-4018-876a-2db732cb57c4">IEnumCERTVIEWEXTENSION::GetFlags</a>
 

 

