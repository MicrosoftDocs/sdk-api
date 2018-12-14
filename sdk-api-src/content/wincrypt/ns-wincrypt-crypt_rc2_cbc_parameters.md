---
UID: NS:wincrypt._CRYPT_RC2_CBC_PARAMETERS
title: CRYPT_RC2_CBC_PARAMETERS
author: windows-sdk-content
description: Contains information used with szOID_RSA_RC2CBC encryption.
old-location: security\crypt_rc2_cbc_parameters.htm
tech.root: seccrypto
ms.assetid: 58b1dc44-55ea-4c22-a115-dfeaee8a2297
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCRYPT_RC2_CBC_PARAMETERS, CRYPT_RC2_128BIT_VERSION, CRYPT_RC2_40BIT_VERSION, CRYPT_RC2_56BIT_VERSION, CRYPT_RC2_64BIT_VERSION, CRYPT_RC2_CBC_PARAMETERS, CRYPT_RC2_CBC_PARAMETERS structure [Security], PCRYPT_RC2_CBC_PARAMETERS, PCRYPT_RC2_CBC_PARAMETERS structure pointer [Security], _crypto2_crypt_rc2_cbc_parameters, security.crypt_rc2_cbc_parameters, wincrypt/CRYPT_RC2_CBC_PARAMETERS, wincrypt/PCRYPT_RC2_CBC_PARAMETERS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_RC2_CBC_PARAMETERS
product: Windows
targetos: Windows
req.typenames: CRYPT_RC2_CBC_PARAMETERS, *PCRYPT_RC2_CBC_PARAMETERS
req.redist: 
---

# CRYPT_RC2_CBC_PARAMETERS structure


## -description


The <b>CRYPT_RC2_CBC_PARAMETERS</b> structure contains information used with szOID_RSA_RC2CBC encryption. It is used in calls to 
<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>, 
<a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a>, 
<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>
<a href="https://msdn.microsoft.com/bf1935f0-1ab0-4068-9ed5-8fbb2c286b8a">CryptDecodeObjectEx</a>.


## -struct-fields




### -field dwVersion

Specifies the key length. Current usable key lengths are 40, 64, and 128 bits. 




<div class="alert"><b>Note</b>  The numeric value of defined constants for <b>dwVersion</b> are not the same as the key lengths they specified. Currently defined values for <b>dwVersion</b> are shown in the following table.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_RC2_40BIT_VERSION"></a><a id="crypt_rc2_40bit_version"></a><dl>
<dt><b>CRYPT_RC2_40BIT_VERSION</b></dt>
<dt>160</dt>
</dl>
</td>
<td width="60%">
40 bits

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_RC2_56BIT_VERSION"></a><a id="crypt_rc2_56bit_version"></a><dl>
<dt><b>CRYPT_RC2_56BIT_VERSION</b></dt>
<dt>52</dt>
</dl>
</td>
<td width="60%">
56 bits

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_RC2_64BIT_VERSION"></a><a id="crypt_rc2_64bit_version"></a><dl>
<dt><b>CRYPT_RC2_64BIT_VERSION</b></dt>
<dt>120</dt>
</dl>
</td>
<td width="60%">
64 bits

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_RC2_128BIT_VERSION"></a><a id="crypt_rc2_128bit_version"></a><dl>
<dt><b>CRYPT_RC2_128BIT_VERSION</b></dt>
<dt>58</dt>
</dl>
</td>
<td width="60%">
128 bits

</td>
</tr>
</table>
 


### -field fIV

Boolean specifying whether an 8-byte <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">initialization vector</a> (IV) is contained in <b>rgbIV[8]</b>. Set to <b>TRUE</b> when IV is present.


### -field rgbIV

Eight byte <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">initialization vector</a>. Can be <b>NULL</b> if fIV is <b>FALSE</b>. The IV is encoded as an OCTET_STRING. 





<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> or 
<a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a> with the <i>dwCertEncodingType</i> parameter set to X500_OCTET_STRING to create the encoded OCTET_STRING. The <b>ContentEncryptionAlgorithm</b>'s <b>Parameters</b> BLOB is updated to point to this encoded OCTET_STRING.

<div class="alert"><b>Note</b>  When a message is decrypted, if it has an IV parameter, the message functions calls 
<a href="https://msdn.microsoft.com/e99a84a2-c23e-4251-8062-dd286ccc29b7">CryptSetKeyParam</a> with the IV before doing the decryption.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a>



<a href="https://msdn.microsoft.com/c683c515-3061-48e3-a64a-2798bd1245b0">CRYPT_ENCRYPT_MESSAGE_PARA</a>



<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>



<a href="https://msdn.microsoft.com/e99a84a2-c23e-4251-8062-dd286ccc29b7">CryptSetKeyParam</a>
 

 

