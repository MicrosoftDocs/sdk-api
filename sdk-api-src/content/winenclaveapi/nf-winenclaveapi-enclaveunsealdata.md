---
UID: NF:winenclaveapi.EnclaveUnsealData
title: EnclaveUnsealData function
author: windows-sdk-content
description: Decrypts an encrypted binary large object (blob).
old-location: base\enclaveunsealdata.htm
tech.root: memory
ms.assetid: DDBDBEDE-E7EA-43B0-B2C7-B85D75EF3EB0
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ENCLAVE_UNSEAL_FLAG_STALE_KEY, EnclaveUnsealData, EnclaveUnsealData function, base.enclaveunsealdata, winenclaveapi/EnclaveUnsealData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - vertdll.dll
api_name:
 - EnclaveUnsealData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnclaveUnsealData function


## -description


Decrypts an encrypted binary large object (blob).


## -parameters




### -param ProtectedBlob [in]

A pointer to the sealed data to unseal.  This data may be stored either within the address range of the enclave or within the address space of the host process


### -param ProtectedBlobSize [in]

The size of the sealed data to unseal, in bytes.


### -param DecryptedData [out]

A pointer to a buffer where the unencrypted data should be placed.  This data may be stored either within the address range of the enclave or within the address space of the host process.  If this  parameter is NULL, only the size of the decrypted data is calculated.


### -param BufferSize [in]

The size of the buffer to which the <i>DecryptedData</i> parameter points, in bytes. If <i>DecryptedData</i> is NULL, <i>BufferSize</i> must be zero.  If <i>DecryptedData</i> is not NULL, and if the size of the decrypted data is larger than this value, an error is returned.


### -param DecryptedDataSize [out]

A pointer to a variable that receives the actual size of the decrypted data, in bytes.


### -param SealingIdentity [out, optional]

 An optional pointer to a buffer that should be filled with the identity of the enclave that sealed the data.  If this pointer is NULL, the  identity of the sealing enclave is  not returned.


### -param UnsealingFlags [out, optional]

An optional pointer to a variable that receives zero or more of the following flags that describe the encrypted binary large object.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_UNSEAL_FLAG_STALE_KEY"></a><a id="enclave_unseal_flag_stale_key"></a><dl>
<dt><b>ENCLAVE_UNSEAL_FLAG_STALE_KEY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
 The data was encrypted with a stale key.  Sealing keys are rotated when required for security, and the system can only maintain a fixed number of recently known keys.  An enclave that determines that data was encrypted with a stale key should reencrypt the data with a current key to minimize the chances that the key used to encrypt the data is no longer maintained in the key list. 

</td>
</tr>
</table>
 


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The enclave that calls <b>EnclaveUnsealData</b> must meet the criteria that correspond to the value of the <a href="https://msdn.microsoft.com/986C122D-4CC9-487F-8B9F-6B3F9B727E4A">ENCLAVE_SEALING_IDENTITY_POLICY</a> that was specified by the enclave that sealed the data by calling <a href="https://msdn.microsoft.com/C5711D43-F0B4-43C6-B0DB-D65622851384">EnclaveSealData</a>.

<b>EnclaveUnsealData</b> must be called from within an enclave, and is only supported within enclaves that have the  <b>ENCLAVE_TYPE_VBS</b> enclave type.




## -see-also




<a href="https://msdn.microsoft.com/986C122D-4CC9-487F-8B9F-6B3F9B727E4A">ENCLAVE_SEALING_IDENTITY_POLICY</a>



<a href="https://msdn.microsoft.com/C5711D43-F0B4-43C6-B0DB-D65622851384">EnclaveSealData</a>
 

 

