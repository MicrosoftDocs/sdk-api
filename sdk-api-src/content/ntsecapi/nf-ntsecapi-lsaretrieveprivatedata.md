---
UID: NF:ntsecapi.LsaRetrievePrivateData
title: LsaRetrievePrivateData function (ntsecapi.h)
description: Do not use the LSA private data functions for generic data encryption and decryption. Instead, use the CryptProtectData and CryptUnprotectData functions. (LsaRetrievePrivateData)
helpviewer_keywords: ["G$","L$","LsaRetrievePrivateData","LsaRetrievePrivateData function [Security]","M$","_lsa_lsaretrieveprivatedata","ntsecapi/LsaRetrievePrivateData","security.lsaretrieveprivatedata"]
old-location: security\lsaretrieveprivatedata.htm
tech.root: security
ms.assetid: 005460db-0919-46eb-b057-37c5b6042243
ms.date: 12/05/2018
ms.keywords: G$, L$, LsaRetrievePrivateData, LsaRetrievePrivateData function [Security], M$, _lsa_lsaretrieveprivatedata, ntsecapi/LsaRetrievePrivateData, security.lsaretrieveprivatedata
req.header: ntsecapi.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaRetrievePrivateData
 - ntsecapi/LsaRetrievePrivateData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-lsapolicy-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaRetrievePrivateData
---

# LsaRetrievePrivateData function


## -description

Do not use the LSA private data functions for generic data encryption and decryption. Instead, use the <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata">CryptProtectData</a> and <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata">CryptUnprotectData</a> functions. Only use the LSA private data functions when it is necessary to manipulate LSA secrets as documented in <a href="/openspecs/windows_protocols/ms-lsad/483f1b6e-7b14-4341-9ab2-9b99c01f896e">Secret Object Data Model</a>

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The handle must have the POLICY_GET_PRIVATE_INFORMATION access right. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param KeyName [in]

Pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the name of the key under which the private data is stored.

To create a specialized object, add one of the following prefixes to the key name.

<table>
<tr>
<th>Prefix</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="L_"></a><a id="l_"></a><dl>
<dt><b>L$</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
For local objects.

</td>
</tr>
<tr>
<td width="40%"><a id="G_"></a><a id="g_"></a><dl>
<dt><b>G$</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
For global objects.

</td>
</tr>
<tr>
<td width="40%"><a id="M_"></a><a id="m_"></a><dl>
<dt><b>M$</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
For computer objects.

</td>
</tr>
</table>
 

If you are not creating one of these specialized types, you do not need to specify a key name prefix. For more information, see 
<a href="/windows/desktop/SecMgmt/private-data-object">Private Data Object</a>.

### -param PrivateData [out]

Pointer to a variable that receives a pointer to an <a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the private data.

When you no longer need the information, pass the returned pointer to 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>.

## -returns

If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> value, which can be the following value or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_OBJECT_NAME_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No private data is stored under the name specified by the <i>KeyName</i> parameter.
							

</td>
</tr>
</table>
 

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> value to a Windows error code.

## -remarks

You must run this process "As Administrator" or the call fails with ERROR_ACCESS_DENIED.

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata">LsaStorePrivateData</a>
