---
UID: NF:wincrypt.CertFindCTLInStore
title: CertFindCTLInStore function
author: windows-sdk-content
description: Finds the first or next certificate trust list (CTL) context that matches search criteria established by the dwFindType and its associated pvFindPara.
old-location: security\certfindctlinstore.htm
old-project: SecCrypto
ms.assetid: e5ed3b22-e96f-4e7d-a20e-eebed0a84d3c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CTL_FIND_ANY, CTL_FIND_EXISTING, CTL_FIND_MD5_HASH, CTL_FIND_SAME_USAGE_FLAG, CTL_FIND_SHA1_HASH, CTL_FIND_SUBJECT, CTL_FIND_USAGE, CertFindCTLInStore, CertFindCTLInStore function [Security], _crypto2_certfindctlinstore, security.certfindctlinstore, wincrypt/CertFindCTLInStore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - CertFindCTLInStore
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertFindCTLInStore function


## -description


The <b>CertFindCTLInStore</b> function finds the first or next <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a> that matches search criteria established by the <i>dwFindType</i> and its associated <i>pvFindPara</i>. This function can be used in a loop to find all of the CTL contexts in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> that match the specified find criteria.


## -parameters




### -param hCertStore [in]

Handle of the certificate store to be searched.


### -param dwMsgAndCertEncodingType [in]

Specifies the type of encoding used on the CTL. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>


This parameter is used only when the <i>dwFindType</i> parameter is set to CTL_FIND_USAGE.


### -param dwFindFlags [in]

Can be set when <i>dwFindType</i> is set to CTL_FIND_USAGE. For details, see the comments under CTL_FIND_USAGE, following.


### -param dwFindType [in]

Specifies the type of search being made. The search type determines the data type, contents, and the use of <i>pvFindPara</i>. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_ANY"></a><a id="ctl_find_any"></a><dl>
<dt><b>CTL_FIND_ANY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <b>NULL</b>.

Any CTL is a match.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_SHA1_HASH"></a><a id="ctl_find_sha1_hash"></a><dl>
<dt><b>CTL_FIND_SHA1_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a>.

A CTL with a hash matching the hash in the <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> structure is found.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_MD5_HASH"></a><a id="ctl_find_md5_hash"></a><dl>
<dt><b>CTL_FIND_MD5_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a>.

A CTL with a hash matching the hash in the <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> structure is found.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_USAGE"></a><a id="ctl_find_usage"></a><dl>
<dt><b>CTL_FIND_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="https://msdn.microsoft.com/bb6a7013-19ec-4263-b7a2-33c79c2b5feb">CTL_FIND_USAGE_PARA</a>.

Any CTL is found that has a usage identifier, list identifier, or signer matching the usage identifier, list identifier, or signer in the <a href="https://msdn.microsoft.com/bb6a7013-19ec-4263-b7a2-33c79c2b5feb">CTL_FIND_USAGE_PARA</a> structure.

If the <b>cUsageIdentifier</b> member is of <b>SubjectUsage</b> size, any CTL is a match.

If the <b>cbData</b> member of <b>ListIdentifier</b> member is zero, any list identifier is a match. If the <b>cbData</b> member of <b>ListIdentifier</b> is CTL_FIND_NO_LIST_ID_CBDATA, only a CTL without a list identifier is a match.

If the <b>pSigner</b> member in the <a href="https://msdn.microsoft.com/bb6a7013-19ec-4263-b7a2-33c79c2b5feb">CTL_FIND_USAGE_PARA</a> structure is <b>NULL</b>, any CTL signer is a match, and only the <b>Issuer</b> and <b>SerialNumber</b> members in the <b>pSigner</b> <a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure are used. If <b>pSigner</b> is CTL_FIND_NO_SIGNER_PTR, only a CTL without a signer is a match.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_SAME_USAGE_FLAG"></a><a id="ctl_find_same_usage_flag"></a><dl>
<dt><b>CTL_FIND_SAME_USAGE_FLAG</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="https://msdn.microsoft.com/bb6a7013-19ec-4263-b7a2-33c79c2b5feb">CTL_FIND_USAGE_PARA</a>.

Only CTLs with exactly the same usage identifiers are matched. CTLs having additional usage identifiers are not matched. For example, if only "1.2.3" is specified in the <a href="https://msdn.microsoft.com/bb6a7013-19ec-4263-b7a2-33c79c2b5feb">CTL_FIND_USAGE_PARA</a> structure, then for a match, the CTL must only contain "1.2.3" and no additional usage identifiers.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_EXISTING"></a><a id="ctl_find_existing"></a><dl>
<dt><b>CTL_FIND_EXISTING</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">PCCTL_CONTEXT</a>.

Searches for the next CRL that is an exact match of the <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_SUBJECT"></a><a id="ctl_find_subject"></a><dl>
<dt><b>CTL_FIND_SUBJECT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="https://msdn.microsoft.com/b3a63010-9025-4a86-aa48-bfb6e800a07a">CTL_FIND_SUBJECT_PARA</a>.

A CTL having the specified subject is found. <a href="https://msdn.microsoft.com/e0c81531-e649-45bb-bafe-bced00c7b16a">CertFindSubjectInCTL</a> can be called to get a pointer to the subject's entry in the CTL. The <b>pUsagePara</b> member in <a href="https://msdn.microsoft.com/b3a63010-9025-4a86-aa48-bfb6e800a07a">CTL_FIND_SUBJECT_PARA</a> can optionally be set to enable the matching described preceding under CTL_FIND_USAGE.

</td>
</tr>
</table>
 


### -param pvFindPara [in]

A pointer to the search value associated with the <i>dwFindType</i> parameter.


### -param pPrevCtlContext [in]

A pointer to the last 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> returned by this function. It must be <b>NULL</b> to get the first CTL in the store. Successive CTLs are retrieved by setting <i>pPrevCtlContext</i> to the pointer to the <b>CTL_CONTEXT</b> returned by a previous function call. Any certificates that do not meet the search criteria or that have been previously deleted by 
<a href="https://msdn.microsoft.com/e24d3445-8929-463a-b771-1f25f4e999b5">CertDeleteCTLFromStore</a> are skipped. This function frees the <b>CTL_CONTEXT</b> referenced by non-<b>NULL</b> values of this parameter.


## -returns



If the function succeeds, the return value is a pointer to a read-only <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CTL</a><a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a>.

For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Either no CTLs were found in the store, no CTL was found matching the search criteria, or the function reached the end of the store's list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hCertStore</i> parameter is not the same as that in the CTL context pointed to by the <i>pPrevCtlContext</i> parameter, or a value that is not valid was specified in the <i>dwFindType</i> parameter.

</td>
</tr>
</table>
 




## -remarks



A returned pointer is freed when passed as the <i>pPrevCtlContext</i> on a subsequent call to the function. Otherwise, the pointer must be freed by calling 
<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>. A non-<b>NULL</b><i>pPrevCtlContext</i> passed to the function is always freed with a call to <b>CertFreeCTLContext</b>, even if the function generates an error.


<a href="https://msdn.microsoft.com/512d246f-9f22-4ac1-a4fc-d5c615a65cf9">CertDuplicateCTLContext</a> can be called to make a duplicate of the returned context. The returned CTL context can be added to a different certificate store using 
<a href="https://msdn.microsoft.com/e8858f75-77a1-4c5f-a3e3-a645c5e0f053">CertAddCTLContextToStore</a>, or a link to that CTL context can be added to a noncollection store using 
<a href="https://msdn.microsoft.com/c129aeae-69d9-440a-979d-e9e481c64538">CertAddCTLLinkToStore</a>. If a CTL matching the search criteria is not found, <b>NULL</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/bb6a7013-19ec-4263-b7a2-33c79c2b5feb">CTL_FIND_USAGE_PARA</a>



<a href="https://msdn.microsoft.com/e8858f75-77a1-4c5f-a3e3-a645c5e0f053">CertAddCTLContextToStore</a>



<a href="https://msdn.microsoft.com/c129aeae-69d9-440a-979d-e9e481c64538">CertAddCTLLinkToStore</a>



<a href="https://msdn.microsoft.com/e24d3445-8929-463a-b771-1f25f4e999b5">CertDeleteCTLFromStore</a>



<a href="https://msdn.microsoft.com/512d246f-9f22-4ac1-a4fc-d5c615a65cf9">CertDuplicateCTLContext</a>



<a href="https://msdn.microsoft.com/dac9f91e-8ed4-43ce-8147-485c2ed7edd5">CertEnumCTLsInStore</a>



<a href="https://msdn.microsoft.com/e0c81531-e649-45bb-bafe-bced00c7b16a">CertFindSubjectInCTL</a>



<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Trust List Functions</a>
 

 

