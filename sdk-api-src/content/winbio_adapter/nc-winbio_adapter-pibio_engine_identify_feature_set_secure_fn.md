---
UID: NC:winbio_adapter.PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN
title: PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN
author: windows-sdk-content
description: Called by the Windows Biometric Framework to build a template from the current feature set and locate a matching template in the database.
old-location: secbiomet\engineadapteridentifyfeaturesetsecure.htm
tech.root: SecBioMet
ms.assetid: 56BD9A75-2779-4D21-A083-75736DE6880E
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EngineAdapterIdentifyFeatureSetSecure, EngineAdapterIdentifyFeatureSetSecure callback function [Windows Biometric Framework API], PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN, PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN callback, secbiomet.engineadapteridentifyfeaturesetsecure, winbio_adapter/EngineAdapterIdentifyFeatureSetSecure
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterIdentifyFeatureSetSecure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN callback function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Called by the Windows Biometric Framework to build a template from the current feature set and locate a matching template in the database. If a match can be found, the engine adapter must fill the <i>Identity</i>, <i>SubFactor</i>, <i>Authorization</i>, and <i>AuthorizationSize</i> fields.


## -parameters




### -param Pipeline

Pointer to a WINBIO_PIPELINE structure associated with the biometric unit performing the operation.


### -param *Nonce

Pointer to a buffer that contains a nonce.


### -param NonceSize

Size, in bytes, of the buffer specified by the <i>Nonce</i> parameter.


### -param *KeyIdentifier

Pointer to a buffer that contains an identifier for the key from a previous call to <a href="https://msdn.microsoft.com/3EB42081-6949-46F8-B235-377234A90C39">EngineAdapterCreateKey</a>



### -param KeyIdentifierSize

Size, in bytes, of the buffer specified by the <i>KeyIdentifier</i> parameter.


### -param Identity

Pointer to a <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure that contains the SID of the template recovered from the database. This value is returned only if a match is found.


### -param SubFactor


### -param RejectDetail

Pointer to a variable that receives additional information if a capture failure prevents the engine from performing a matching operation. If the most recent capture succeeded, set this parameter to zero.


### -param *Authorization

An HMAC. See remarks section.


### -param AuthorizationSize

Size, in bytes, of the buffer specified by the <i>Authorization</i> parameter.


#### - Subfactor

A <a href="https://msdn.microsoft.com/019569A9-6184-4E75-9B82-C98F4F45F61A">WINBIO_BIOMETRIC_SUBTYPE Constants</a> value that receives the sub-factor associated with the template in the database. See the Remarks section for more details. This value is returned only if a match is found.


## -returns



<b>WINBIO_E_INVALID_KEY_IDENTIFIER</b> must be returned in the case where the key cannot be used for whatever reason. When <b>WINBIO_E_INVALID_KEY_IDENTIFIER </b>is returned, the sensor and TPM will be re-provisioned.




## -remarks



The Authorization buffer contains the following SHA256_HMAC:

SHA256_HMAC(Key, SHA256(Nonce || 0xffffffe2 || SHA256(AccountSid)))

<ul>
<li>
Key

Key is the HMAC key passed in by <a href="https://msdn.microsoft.com/3EB42081-6949-46F8-B235-377234A90C39">EngineAdapterCreateKey</a>, and identified by the <i>KeyIdentifier</i> parameter.

</li>
<li>
Nonce

Nonce is the Nonce parameter.

</li>
<li>
0xffffffe2

A 32-bit unsigned integer in big-endian format.

</li>
<li>
AccountSid

The account SID of the user referenced by the Identity parameter. The SID bytes can be obtained from the <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure.

</li>
</ul>

#### Examples

Here is a pseudocode implementation of the SHA256 HMAC calculation:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>// Hash the AccountSid.
    assert(Identity-&gt;Type == WINBIO_ID_TYPE_SID);
    hashHandle = CreateHash(SHA256_ALGORITHM);
    HashData(
        hashHandle, 
        Identity-&gt;Value.AccountSid.Data, 
        Identity-&gt;Value.AccountSid.Size);
    identityHash = FinishHash(hashHandle);

    // Hash the parameters.
    BYTE bytes[] = {0xff, 0xff, 0xff, 0xe2};
    hashHandle = CreateHash(SHA256_ALGORITHM);
    HashData(hashHandle, Nonce, NonceSize);
    HashData(hashHandle, bytes, sizeof(bytes));
    HashData(hashHandle, identityHash, SHA256_DIGEST_LENGTH);
    parameterHash = FinishHash(hashHandle);

    // Calculate the authorization HMAC
    key, keySize = GetKeyFromIdentifier(KeyIdentifier, KeyIdentifierSize);
    hashHandle = CreateHash(HMAC_SHA256_ALGORITHM, key, keySize);
    HashData(hashHandle, parameterHash, SHA256_DIGEST_LENGTH);
    authorization = FinishHash(hashHandle);
</pre>
</td>
</tr>
</table></span></div>


