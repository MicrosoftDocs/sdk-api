---
UID: NF:ntsecapi.LsaStorePrivateData
title: LsaStorePrivateData function (ntsecapi.h)
description: Do not use the LSA private data functions for generic data encryption and decryption. Instead, use the CryptProtectData and CryptUnprotectData functions. Only use the LSA private data functions when it is necessary to manipulate LSA secrets  (LsaStorePrivateData)
helpviewer_keywords: ["LsaStorePrivateData","LsaStorePrivateData function [Security]","_lsa_lsastoreprivatedata","ntsecapi/LsaStorePrivateData","security.lsastoreprivatedata"]
old-location: security\lsastoreprivatedata.htm
tech.root: security
ms.assetid: 95d6cf30-fd08-473e-b0b3-3f7ca5e85357
ms.date: 12/05/2018
ms.keywords: LsaStorePrivateData, LsaStorePrivateData function [Security], _lsa_lsastoreprivatedata, ntsecapi/LsaStorePrivateData, security.lsastoreprivatedata
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
 - LsaStorePrivateData
 - ntsecapi/LsaStorePrivateData
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
 - LsaStorePrivateData
---

# LsaStorePrivateData function


## -description

Do not use the LSA private data functions or generic data encryption and decryption. Instead, use the <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata">CryptProtectData</a> and <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata">CryptUnprotectData</a> functions. Only use the LSA private data functions when it is necessary to manipulate LSA secrets as documented in <a href="/openspecs/windows_protocols/ms-lsad/483f1b6e-7b14-4341-9ab2-9b99c01f896e">Secret Object Data Model</a>

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The handle must have the POLICY_CREATE_SECRET access right if this is the first time data is being stored under the key specified by the <i>KeyName</i> parameter. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param KeyName [in]

Pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure containing the name of the key under which the private data is stored.

### -param PrivateData [in]

Pointer to an <a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure containing the private data to store. The function encrypts this data before storing it.

If this parameter is <b>NULL</b>, the function deletes any private data stored under the key and deletes the key. Subsequent attempts to retrieve data from the key will return the STATUS_OBJECT_NAME_NOT_FOUND error code.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -remarks

The <b>LsaStorePrivateData</b> function can be used by server applications to store client and machine passwords.

As described in 
<a href="/windows/desktop/SecMgmt/private-data-object">Private Data Object</a>, private data objects include three specialized types: local, global, and machine. Specialized objects are identified by a prefix in the key name: "L$" for local objects, "G$" for global objects, and "M$" for machine objects. Local objects cannot be accessed remotely. Machine objects can be accessed only by the operating system.

In addition to these prefixes, the following values also indicate local or machine objects. These values are supported for backward compatibility and should not be used when you create new local or machine objects. The key name of local private data objects may also be "$machine.acc", "SAC", "SAI", "SANSC", or start with "RasDialParms" or "RasCredentials". The key name for machine objects may also start with, "NL$" or "_sc_".

Private data objects which do not use any of the preceding key name conventions can be accessed remotely and are not replicated to other domains.

The data stored by the <b>LsaStorePrivateData</b> function is not absolutely protected. However, the data is encrypted before being stored, and the key has a <a href="/windows/desktop/SecGloss/d-gly">DACL</a> that allows only the creator and administrators to read the data.

Use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaretrieveprivatedata">LsaRetrievePrivateData</a> function to retrieve the value stored by <b>LsaStorePrivateData</b>.

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaretrieveprivatedata">LsaRetrievePrivateData</a>
