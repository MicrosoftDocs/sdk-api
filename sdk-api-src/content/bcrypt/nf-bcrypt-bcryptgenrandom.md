---
UID: NF:bcrypt.BCryptGenRandom
title: BCryptGenRandom function (bcrypt.h)
description: Generates a random number.
helpviewer_keywords: ["BCRYPT_RNG_USE_ENTROPY_IN_BUFFER","BCRYPT_USE_SYSTEM_PREFERRED_RNG","BCryptGenRandom","BCryptGenRandom function [Security]","bcrypt/BCryptGenRandom","security.bcryptgenrandom_func"]
old-location: security\bcryptgenrandom_func.htm
tech.root: security
ms.assetid: 7c6cee3a-f2c5-46f3-8cfe-984316f323d9
ms.date: 12/05/2018
ms.keywords: BCRYPT_RNG_USE_ENTROPY_IN_BUFFER, BCRYPT_USE_SYSTEM_PREFERRED_RNG, BCryptGenRandom, BCryptGenRandom function [Security], bcrypt/BCryptGenRandom, security.bcryptgenrandom_func
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib or Cng.lib(For Kernel mode)
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptGenRandom
 - bcrypt/BCryptGenRandom
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptGenRandom
---

# BCryptGenRandom function


## -description

The <b>BCryptGenRandom</b> function generates a random number.

## -parameters

### -param hAlgorithm [in, out]

The handle of an algorithm provider created by using the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a> function. The algorithm that was specified when the provider was created must support the random number generator interface.

### -param pbBuffer [in, out]

The address of a buffer that receives the random number. The size of this buffer is specified by the <i>cbBuffer</i> parameter.

### -param cbBuffer [in]

The size, in bytes, of the <i>pbBuffer</i> buffer.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. This parameter can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RNG_USE_ENTROPY_IN_BUFFER"></a><a id="bcrypt_rng_use_entropy_in_buffer"></a><dl>
<dt><b>BCRYPT_RNG_USE_ENTROPY_IN_BUFFER</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
This function will use the number in the <i>pbBuffer</i> buffer as additional entropy for the random number. If this flag is not specified, this function will use a random number for the entropy.

<b>Windows 8 and later:  </b>This flag is ignored in  Windows 8 and later.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_USE_SYSTEM_PREFERRED_RNG"></a><a id="bcrypt_use_system_preferred_rng"></a><dl>
<dt><b>BCRYPT_USE_SYSTEM_PREFERRED_RNG</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Use the system-preferred random number generator algorithm. The <i>hAlgorithm</i> parameter must be <b>NULL</b>.

BCRYPT_USE_SYSTEM_PREFERRED_RNG is only supported at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a>. For more information, see Remarks.

<b>Windows Vista:  </b>This flag is not supported without SP2.

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
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hAlgorithm</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
</table>

## -remarks

The default random number provider implements an algorithm for generating random numbers that complies with the NIST SP800-90 standard, specifically the  CTR_DRBG portion of that standard.

<b>Windows Vista:  </b>Prior to Windows Vista with Service Pack 1 (SP1) the default random number provider implements an algorithm for generating random numbers that complies with the FIPS 186-2 standard. 

When using a supported algorithm provider, <b>BCryptGenRandom</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hAlgorithm</i> parameter must have been opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptGenRandom</b> function must refer to nonpaged (or locked) memory. <b>Windows Vista:  </b>The Microsoft provider does not support calling at <b>DISPATCH_LEVEL</b>.



To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.
