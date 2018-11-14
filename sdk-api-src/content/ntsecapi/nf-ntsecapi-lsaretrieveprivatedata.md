---
UID: NF:ntsecapi.LsaRetrievePrivateData
title: LsaRetrievePrivateData function
author: windows-sdk-content
description: Do not use the LSA private data functions. Instead, use the CryptProtectData and CryptUnprotectData functions.
old-location: security\lsaretrieveprivatedata.htm
tech.root: secmgmt
ms.assetid: 005460db-0919-46eb-b057-37c5b6042243
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: G$, L$, LsaRetrievePrivateData, LsaRetrievePrivateData function [Security], M$, _lsa_lsaretrieveprivatedata, ntsecapi/LsaRetrievePrivateData, security.lsaretrieveprivatedata
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
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
 - LsaRetrievePrivateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- LsaRetrievePrivateData
: 
---

# LsaRetrievePrivateData function


## -description


Do not use the LSA private data functions. Instead, use the <a href="https://msdn.microsoft.com/765a68fd-f105-49fc-a738-4a8129eb0770">CryptProtectData</a> and <a href="https://msdn.microsoft.com/54eab3b0-d341-47c6-9c32-79328d7a7155">CryptUnprotectData</a> functions.  


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The handle must have the POLICY_GET_PRIVATE_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param KeyName [in]

Pointer to an 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the name of the key under which the private data is stored.

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
<a href="https://msdn.microsoft.com/927473d7-b5bc-4b6f-b303-8a0f8680731d">Private Data Object</a>.


### -param PrivateData [out]

Pointer to a variable that receives a pointer to an <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the private data.

When you no longer need the information, pass the returned pointer to 
<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> value, which can be the following value or one of the 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

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
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> value to a Windows error code.




## -remarks



You must run this process "As Administrator" or the call fails with ERROR_ACCESS_DENIED.




## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>



<a href="https://msdn.microsoft.com/95d6cf30-fd08-473e-b0b3-3f7ca5e85357">LsaStorePrivateData</a>
 

 

