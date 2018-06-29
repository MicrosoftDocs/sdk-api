---
UID: NF:ntsecapi.LsaStorePrivateData
title: LsaStorePrivateData function
author: windows-sdk-content
description: Do not use the LSA private data functions. Instead, use the CryptProtectData and CryptUnprotectData functions.
old-location: security\lsastoreprivatedata.htm
old-project: SecMgmt
ms.assetid: 95d6cf30-fd08-473e-b0b3-3f7ca5e85357
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: LsaStorePrivateData, LsaStorePrivateData function [Security], _lsa_lsastoreprivatedata, ntsecapi/LsaStorePrivateData, security.lsastoreprivatedata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaStorePrivateData
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# LsaStorePrivateData function


## -description



			Do not use the LSA private data functions. Instead, use the <a href="https://msdn.microsoft.com/765a68fd-f105-49fc-a738-4a8129eb0770">CryptProtectData</a> and <a href="https://msdn.microsoft.com/54eab3b0-d341-47c6-9c32-79328d7a7155">CryptUnprotectData</a> functions.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The handle must have the POLICY_CREATE_SECRET access right if this is the first time data is being stored under the key specified by the <i>KeyName</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param KeyName [in]

Pointer to an 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure containing the name of the key under which the private data is stored.


### -param PrivateData [in]

Pointer to an <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure containing the private data to store. The function encrypts this data before storing it.

If this parameter is <b>NULL</b>, the function deletes any private data stored under the key and deletes the key. Subsequent attempts to retrieve data from the key will return the STATUS_OBJECT_NAME_NOT_FOUND error code.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://msdn.microsoft.com/library/ms721859(v=VS.85).aspx">LSA Policy Function Return Values</a>.

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -remarks



The <b>LsaStorePrivateData</b> function can be used by server applications to store client and machine passwords.

As described in 
<a href="https://msdn.microsoft.com/927473d7-b5bc-4b6f-b303-8a0f8680731d">Private Data Object</a>, private data objects include three specialized types: local, global, and machine. Specialized objects are identified by a prefix in the key name: "L$" for local objects, "G$" for global objects, and "M$" for machine objects. Local objects cannot be accessed remotely. Machine objects can be accessed only by the operating system.

In addition to these prefixes, the following values also indicate local or machine objects. These values are supported for backward compatibility and should not be used when you create new local or machine objects. The key name of local private data objects may also be "$machine.acc", "SAC", "SAI", "SANSC", or start with "RasDialParms" or "RasCredentials". The key name for machine objects may also start with, "NL$" or "_sc_".

Private data objects which do not use any of the preceding key name conventions can be accessed remotely and are not replicated to other domains.

The data stored by the <b>LsaStorePrivateData</b> function is not absolutely protected. However, the data is encrypted before being stored, and the key has a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">DACL</a> that allows only the creator and administrators to read the data.

Use the 
<a href="https://msdn.microsoft.com/005460db-0919-46eb-b057-37c5b6042243">LsaRetrievePrivateData</a> function to retrieve the value stored by <b>LsaStorePrivateData</b>.




## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/005460db-0919-46eb-b057-37c5b6042243">LsaRetrievePrivateData</a>
 

 

