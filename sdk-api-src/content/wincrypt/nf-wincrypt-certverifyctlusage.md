---
UID: NF:wincrypt.CertVerifyCTLUsage
title: CertVerifyCTLUsage function
author: windows-sdk-content
description: Verifies that a subject is trusted for a specified usage by finding a signed and time-valid certificate trust list (CTL) with the usage identifiers that contain the subject.
old-location: security\certverifyctlusage.htm
old-project: SecCrypto
ms.assetid: d87d8157-8e52-4198-bfd4-46d83d72eb13
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CertVerifyCTLUsage, CertVerifyCTLUsage function [Security], _crypto2_certverifyctlusage, security.certverifyctlusage, wincrypt/CertVerifyCTLUsage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertVerifyCTLUsage
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertVerifyCTLUsage function


## -description


The <b>CertVerifyCTLUsage</b> function verifies that a subject is trusted for a specified usage by finding a signed and time-valid <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) with the usage identifiers that contain the subject. A certificate's subject can be identified by either its <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> or any unique identifier such as the SHA1 <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the subject's certificate.


## -parameters




### -param dwEncodingType [in]

Specifies the encoding type used. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types can be added in the future. For either current encoding type, use  


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.


### -param dwSubjectType [in]

If the <i>dwSubjectType</i> parameter is set to CTL_CERT_SUBJECT_TYPE, <i>pvSubject</i> points to a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure. The structure's <b>SubjectAlgorithm</b> member is examined to determine the representation of the subject's identity. Initially, only SHA1 and MD5 hashes are supported as values for <b>SubjectAlgorithm</b>. The appropriate hash property is obtained from the <b>CERT_CONTEXT</b> structure.

If the <i>dwSubjectType</i> parameter is set to CTL_ANY_SUBJECT_TYPE, <i>pvSubject</i> points to the 
<a href="https://msdn.microsoft.com/367e9914-b69b-47ad-a20a-3dd067708787">CTL_ANY_SUBJECT_INFO</a> structure. The <b>SubjectAlgorithm</b> member of this structure must match the algorithm type of the CTL, and the <b>SubjectIdentifier</b> member must match one of the CTL entries.

If <i>dwSubjectType</i> is set to either preceding value, <i>dwEncodingType</i> is not used.


### -param pvSubject [in]

Value used in conjunction with the <i>dwSubjectType</i> parameter.


### -param pSubjectUsage [in]

A pointer to a 
<a href="https://msdn.microsoft.com/70ee138a-df94-4fc4-9de5-0d8b7704b890">CTL_USAGE</a> structure used to specify the intended usage of the subject.


### -param dwFlags [in]

If the CERT_VERIFY_INHIBIT_CTL_UPDATE_FLAG is not set, a CTL whose time is no longer valid in one of the stores specified by <b>rghCtlStore</b> in 
<a href="https://msdn.microsoft.com/bf9a3c81-f8c4-45a6-b045-8cbefebebbd3">CTL_VERIFY_USAGE_PARA</a> can be replaced. When replaced, the CERT_VERIFY_UPDATED_CTL_FLAG is set in the  <b>dwFlags</b> member of <i>pVerifyUsageStatus</i>. If this flag is set, an update will not be made, even if a time-valid, updated CTL is received for a CTL that is in the store and whose time is no longer valid.

If the CERT_VERIFY_TRUSTED_SIGNERS_FLAG is set, only the signer stores specified by <b>rghSignerStore</b> in 
<a href="https://msdn.microsoft.com/bf9a3c81-f8c4-45a6-b045-8cbefebebbd3">CTL_VERIFY_USAGE_PARA</a> are searched to find the signer. Otherwise, the signer stores provide additional sources to find the signer's certificate. For more information, see Remarks.

If CERT_VERIFY_NO_TIME_CHECK_FLAG is set, the CTLs are not checked for time validity. Otherwise, they are.

If CERT_VERIFY_ALLOW_MORE_USAGE_FLAG is set, the CTL can contain usage identifiers in addition to those specified by <i>pSubjectUsage</i>. Otherwise, the found CTL will contain no additional usage identifiers.


### -param pVerifyUsagePara [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/bf9a3c81-f8c4-45a6-b045-8cbefebebbd3">CTL_VERIFY_USAGE_PARA</a> structure that specifies the stores to be searched to find the CTL and the stores that contain acceptable CTL signers. Setting the <b>ListIdentifier</b> member further limits the search.


### -param pVerifyUsageStatus [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/2b7ef953-9422-4dcf-b293-a78a06bb080e">CTL_VERIFY_USAGE_STATUS</a> structure. The <b>cbSize</b> member of the structure must to be set to the size, in bytes, of the structure, and all other fields must be set to zero before <b>CertVerifyCTLUsage</b> is called. For more information, see 
<b>CTL_VERIFY_USAGE_STATUS</b>.


## -returns



If the subject is trusted for the specified usage, <b>TRUE</b> is returned. Otherwise, <b>FALSE</b> is returned. <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can return one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_VERIFY_USAGE_DLL</b></dt>
</dl>
</td>
<td width="60%">
No DLL or exported function was found to verify subject usage.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_VERIFY_USAGE_CHECK</b></dt>
</dl>
</td>
<td width="60%">
The called function was not able to do a usage check on the subject.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_VERIFY_USAGE_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The server was offline; therefore, the called function could not complete the usage check.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_IN_CTL</b></dt>
</dl>
</td>
<td width="60%">
The subject was not found in a CTL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_TRUSTED_SIGNER</b></dt>
</dl>
</td>
<td width="60%">
No trusted signer was found to verify the signature of the message or trust list.

</td>
</tr>
</table>
 

The <b>dwError</b> member of the <a href="https://msdn.microsoft.com/bf9a3c81-f8c4-45a6-b045-8cbefebebbd3">CTL_VERIFY_USAGE_PARA</a> pointed to by <i>pVerifyUsageStatus</i> is set to the same error code.




## -remarks



<b>CertVerifyCTLUsage</b> is a dispatcher to functions that can be installed by using an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID). First, it tries to find an OID function that matches the first usage object identifier in the <a href="https://msdn.microsoft.com/70ee138a-df94-4fc4-9de5-0d8b7704b890">CLT_USAGE</a> structure pointed to by <i>pSubjectUsage</i>. If this fails, it uses the default <b>CertDllVerifyCTLUsage</b> functions.

The <b>CertDllVerifyCTLUsage</b> function in Cryptnet.dll can be installed by using an OID; it has the following properties:

<ul>
<li>If CTL stores are specified by <b>rghCtlStore</b> in <i>pVerifyUsagePara</i>, only those stores are searched to find a CTL. Otherwise, the Trust system store is searched to find a CTL.</li>
<li>If CERT_VERIFY_TRUSTED_SIGNERS_FLAG is set, only the signer stores specified by <b>rghSignerStore</b> in <i>pVerifyUsagePara</i> are searched to find the certificate that corresponds to the signer's issuer and serial number. Otherwise, the CTL message's store, the signer stores specified by <b>rghSignerStore</b> in <i>pVerifyUsagePara</i>, the Trust system store, CA system store, ROOT, and <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Software Publisher Certificate</a> (SPC) system stores are searched to find the signer's certificate. In either case, the public key in the found certificate is used to verify the signature of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CTL</a>.</li>
<li>If the CTL has a set <b>NextUpdate</b> member and CERT_VERIFY_NO_TIME_CHECK is not set, it is verified for time validity.</li>
<li>If the CTL obtained from the store has a time that is not valid, an attempt is made to get a time-valid version. The <b>CertDllVerifyCTLUsage</b> function uses the <b>NextUpdateLocation</b> property or the <b>NextUpdateLocation</b> extension of the CTL, or it searches the signer's information for a <b>NextUpdateLocation</b> attribute.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/bf9a3c81-f8c4-45a6-b045-8cbefebebbd3">CTL_VERIFY_USAGE_PARA</a>



<a href="https://msdn.microsoft.com/2b7ef953-9422-4dcf-b293-a78a06bb080e">CTL_VERIFY_USAGE_STATUS</a>



<a href="https://msdn.microsoft.com/e5ed3b22-e96f-4e7d-a20e-eebed0a84d3c">CertFindCTLInStore</a>



<a href="https://msdn.microsoft.com/e0c81531-e649-45bb-bafe-bced00c7b16a">CertFindSubjectInCTL</a>



<a href="cryptography_functions.htm">Verification Functions Using CTLs</a>
 

 

