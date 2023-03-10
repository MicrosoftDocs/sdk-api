---
UID: NF:winenclaveapi.EnclaveSealData
title: EnclaveSealData function (winenclaveapi.h)
description: Generates an encrypted binary large object (blob) from unencypted data.
helpviewer_keywords: ["ENCLAVE_RUNTIME_POLICY_ALLOW_DYNAMIC_DEBUG","ENCLAVE_RUNTIME_POLICY_ALLOW_FULL_DEBUG","EnclaveSealData","EnclaveSealData function","base.enclavesealdata","winenclaveapi/EnclaveSealData"]
old-location: base\enclavesealdata.htm
tech.root: base
ms.assetid: C5711D43-F0B4-43C6-B0DB-D65622851384
ms.date: 12/05/2018
ms.keywords: ENCLAVE_RUNTIME_POLICY_ALLOW_DYNAMIC_DEBUG, ENCLAVE_RUNTIME_POLICY_ALLOW_FULL_DEBUG, EnclaveSealData, EnclaveSealData function, base.enclavesealdata, winenclaveapi/EnclaveSealData
req.header: winenclaveapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
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
req.lib: Vertdll.lib
req.dll: Vertdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnclaveSealData
 - winenclaveapi/EnclaveSealData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - vertdll.dll
api_name:
 - EnclaveSealData
---

# EnclaveSealData function


## -description

Generates an encrypted binary large object (blob) from unencypted data.

## -parameters

### -param DataToEncrypt [in]

A pointer to the data that you want to seal. This data can be stored either within the address range of the enclave or within the address range of the host process.

### -param DataToEncryptSize [in]

The size of the data that you want to seal, in bytes.

### -param IdentityPolicy [in]

A value that specifies how another enclave must be related to the enclave that calls <b>EnclaveSealData</b> for the enclave to unseal the data.

### -param RuntimePolicy [in]

A value that indicates whether an enclave that runs with debugging turned on is permitted to unseal the data the this call to <b>EnclaveSealData</b> seals.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_RUNTIME_POLICY_ALLOW_FULL_DEBUG"></a><a id="enclave_runtime_policy_allow_full_debug"></a><dl>
<dt><b>ENCLAVE_RUNTIME_POLICY_ALLOW_FULL_DEBUG</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
 If specified, indicates that an enclave that runs with debugging turned on is permitted to unseal the data.  If not specified, indicates that an enclave that runs with debugging turned on is not permitted to unseal the data.  This flag is automatically included if the calling enclave is running with debugging turned on. 



</td>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_RUNTIME_POLICY_ALLOW_DYNAMIC_DEBUG"></a><a id="enclave_runtime_policy_allow_dynamic_debug"></a><dl>
<dt><b>ENCLAVE_RUNTIME_POLICY_ALLOW_DYNAMIC_DEBUG</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
If specified, indicates that an enclave that runs with dynamic debugging turned on is permitted to unseal the data.  If not specified, indicates that an enclave that runs with dynamic debugging turned on is not permitted to unseal the data.  This flag is automatically included if the calling enclave is running with dynamic debugging turned on

</td>
</tr>
</table>

### -param ProtectedBlob [out]

A pointer to a buffer where the sealed data should be placed.  This data may be stored either within the address range of the enclave or within the address space of the host process.  If this parameter is NULL, only the size of the protected blob is calculated.

### -param BufferSize [in]

 A pointer to a variable that holds the size of the buffer to which the <i>ProtectedBlob</i> parameter points.  If <i>ProtectedBlob</i> is NULL, this value must be zero.  If <i>ProtectedBlob</i> is not NULL, and if the size of the encrypted data is larger than this value, an error occurs.

### -param ProtectedBlobSize [out]

 A pointer to a variable that receives the actual size of the encrypted blob.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>EnclaveSealData</b> must be called from within an enclave, and is only supported within enclaves that have the  <b>ENCLAVE_TYPE_VBS</b> enclave type.

## -see-also

<a href="/windows/desktop/api/ntenclv/ne-ntenclv-enclave_sealing_identity_policy">ENCLAVE_SEALING_IDENTITY_POLICY</a>



<a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveunsealdata">EnclaveUnsealData</a>