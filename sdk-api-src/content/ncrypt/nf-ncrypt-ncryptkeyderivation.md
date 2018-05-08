---
UID: NF:ncrypt.NCryptKeyDerivation
title: NCryptKeyDerivation function
author: windows-driver-content
description: Creates a key from another key by using the specified key derivation function.
old-location: security\ncryptkeyderivation.htm
old-project: SecCNG
ms.assetid: 5D2D61B1-022E-412F-A19E-11057930A615
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: BCRYPT_CAPI_AES_FLAG, NCRYPT_SILENT_FLAG, NCryptKeyDerivation, NCryptKeyDerivation function [Security], ncrypt/NCryptKeyDerivation, security.ncryptkeyderivation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SESSION_HEADER, *PSESSION_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ncrypt.dll
api_name:
-	NCryptKeyDerivation
product: Windows
targetos: Windows
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# NCryptKeyDerivation function


## -description


The <b>NCryptKeyDerivation</b> function creates a key from another key by using the specified key derivation function.  The function returns the key in a byte array.


## -parameters




### -param hKey [in]

Handle of the key derivation function (KDF) key.


### -param pParameterList [in]

The address of a <a href="https://msdn.microsoft.com/ae4673ab-81cd-4604-bafa-8d8c66003aba">NCryptBufferDesc</a> structure that contains the KDF parameters. The parameters can be specific to a KDF or generic. The following table shows the required and optional parameters for specific KDFs implemented by the Microsoft software key storage provider.

<table>
<tr>
<th>KDF</th>
<th>Parameter</th>
<th>Required</th>
</tr>
<tr>
<td>SP800-108 HMAC in counter mode</td>
<td>KDF_LABEL</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_CONTEXT</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_HASH_ALGORITHM</td>
<td>yes</td>
</tr>
<tr>
<td>SP800-56A</td>
<td>KDF_ALGORITHMID</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_PARTYUINFO</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_PARTYVINFO</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_HASH_ALGORITHM</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_SUPPPUBINFO</td>
<td>no</td>
</tr>
<tr>
<td></td>
<td>KDF_SUPPPRIVINFO</td>
<td>no</td>
</tr>
<tr>
<td>PBKDF2</td>
<td>KDF_HASH_ALGORITHM</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_SALT</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_ITERATION_COUNT</td>
<td>no</td>
</tr>
<tr>
<td>CAPI_KDF</td>
<td>KDF_HASH_ALGORITHM</td>
<td>yes</td>
</tr>
</table>
 

The following generic parameter can be used:<ul>
<li>KDF_GENERIC_PARAMETER</li>
</ul>Generic parameters map to KDF specific parameters in the following manner:

SP800-108 HMAC in counter mode:<ul>
<li>KDF_GENERIC_PARAMETER = KDF_LABEL||0x00||KDF_CONTEXT</li>
</ul>


SP800-56A<ul>
<li>KDF_GENERIC_PARAMETER = KDF_ALGORITHMID || KDF_PARTYUINFO || KDF_PARTYVINFO {|| KDF_SUPPPUBINFO } {|| KDF_SUPPPRIVINFO }</li>
</ul>


PBKDF2<ul>
<li>KDF_GENERIC_PARAMETER = KDF_SALT </li>
<li>KDF_ITERATION_COUNT – defaults to 10000</li>
</ul>


CAPI_KDF<ul>
<li>KDF_GENERIC_PARAMETER = Not Used </li>
</ul>



### -param pbDerivedKey [out]

Address of a buffer that receives the key. The <i>cbDerivedKey</i> parameter contains the size, in bytes, of the key buffer.


### -param cbDerivedKey [in]

Size, in bytes, of the buffer pointed to by the <i>pbDerivedKey</i> parameter.


### -param pcbResult [out]

Pointer to a <b>DWORD</b> that receives the number of bytes copied to the buffer pointed to by the <i>pbDerivedKey</i> parameter.


### -param dwFlags [in]

Flags that modify function behavior. The following value can be used with the Microsoft software key storage provider.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_CAPI_AES_FLAG"></a><a id="bcrypt_capi_aes_flag"></a><dl>
<dt><b>BCRYPT_CAPI_AES_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the target algorithm is AES and that the key therefore must be double expanded.
This flag is only valid with the CAPI_KDF algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key service provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the <b>NTE_SILENT_CONTEXT</b> error code as the last error.

</td>
</tr>
</table>
 


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hProvider</i> or <i>hKey</i> handles are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The  <i>pwszDerivedKeyAlg</i> and <i>pParameterList</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory to create the key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not supported by the key storage provider.

</td>
</tr>
</table>
 




## -remarks



You can use the following algorithm identifiers in the <a href="https://msdn.microsoft.com/eeb1842f-fd9e-4edf-9db8-7b4e91760e9b">NCryptCreatePersistedKey</a> function before calling <b>NCryptKeyDerivation</b>:

<ul>
<li><b>BCRYPT_CAPI_KDF_ALGORITHM</b></li>
<li><b>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</b></li>
<li><b>BCRYPT_SP80056A_CONCAT_ALGORITHM</b></li>
<li><b>BCRYPT_PBKDF2_ALGORITHM</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/D0B91FFE-2E72-4AE3-A84F-DC598C02CF53">BCryptKeyDerivation</a>



<a href="https://msdn.microsoft.com/0ff08c6a-5f30-43ca-9db8-cda3e0704b0a">NCryptDeriveKey</a>
 

 

