---
UID: NF:enclaveapi.InitializeEnclave
title: InitializeEnclave function (enclaveapi.h)
description: Initializes an enclave that you created and loaded with data.
helpviewer_keywords: ["InitializeEnclave","InitializeEnclave function","base.initializeenclave","enclaveapi/InitializeEnclave"]
old-location: base\initializeenclave.htm
tech.root: base
ms.assetid: 6A711135-A522-40AE-965F-E1AF97D0076A
ms.date: 5/18/2022
ms.keywords: InitializeEnclave, InitializeEnclave function, base.initializeenclave, enclaveapi/InitializeEnclave
req.header: enclaveapi.h
req.include-header: Winbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Api-ms-win-core-enclave-l1-1-0.dll; Kernel32.dll; KernelBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitializeEnclave
 - enclaveapi/InitializeEnclave
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-enclave-l1-1-0.dll
 - kernel32.dll
 - KernelBase.dll
 - API-MS-Win-Core-Enclave-L1-1-0.dll
api_name:
 - InitializeEnclave
---

# InitializeEnclave function

## -description

Initializes an enclave that you created and loaded with data.

## -parameters

### -param hProcess [in]

A handle to the process for which the enclave was created.

### -param lpAddress [in]

Any address within the enclave.

### -param lpEnclaveInformation [in]

A pointer to architecture-specific information to use to initialize the enclave.

For the **ENCLAVE_TYPE_SGX** and **ENCLAVE_TYPE_SGX2** enclave types, specify a pointer to an [ENCLAVE_INIT_INFO_SGX](/windows/win32/api/winnt/ns-winnt-enclave_init_info_sgx) structure.

For the **ENCLAVE_TYPE_VBS** enclave type, specify a pointer to an [ENCLAVE_INIT_INFO_VBS](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs) structure.

### -param dwInfoLength [in]

The length of the structure that the _lpEnclaveInformation_ parameter points to, in bytes. For the **ENCLAVE_TYPE_SGX** and **ENCLAVE_TYPE_SGX2** enclave types, this value must be 4096. For the **ENCLAVE_TYPE_VBS** enclave type, this value must be `sizeof(ENCLAVE_INIT_INFO_VBS)`, which is 8 bytes.

### -param lpEnclaveError [in]

An optional pointer to  a variable that receives an enclave error code that is architecture-specific.

For the **ENCLAVE_TYPE_SGX** and **ENCLAVE_TYPE_SGX2** enclave types, the _lpEnclaveError_ parameter contains the error that the EINIT instruction generated if the function fails and [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR_ENCLAVE_FAILURE**.

For the **ENCLAVE_TYPE_VBS** enclave type, the _lpEnclaveError_ parameter  is not used.

## -returns

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

For a list of common error codes, see [System Error Codes](/windows/win32/Debug/system-error-codes). The following error codes also apply for this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_ENCLAVE_FAILURE</b></b></dt>
</dl>
</td>
<td width="60%">
An failure specific to the underlying enclave architecture occurred. The value for the <i>lpEnclaveError</i> parameter contains the architecture-specific error.

For the <b>ENCLAVE_TYPE_SGX</b> and <b>ENCLAVE_TYPE_SGX2</b> enclave types, the EINIT instruction that the <a href="/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx">ENCLAVE_INIT_INFO_SGX</a> structure specified generated an error. The value of the <i>lpEnclaveError</i> parameter contains the error that the instruction generated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_BAD_LENGTH</b></b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>dwInfoLength</i> parameter did not match the value expected based on the value specified for the <i>lpEnclaveInformation</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_RETRY</b></b></dt>
</dl>
</td>
<td width="60%">
The processor was not able to initialize the enclave in a timely fashion. Try  to initialize the enclave again.

</td>
</tr>
</table>

## -remarks

To create an enclave, use the [CreateEnclave](nf-enclaveapi-createenclave.md) function. To load data into the enclave before you initialize it, use the [LoadEnclaveData](nf-enclaveapi-loadenclavedata.md) function.

**Windows 10, version 1709 and later and Windows 11:** To delete the enclave when you finish using it, call [DeleteEnclave](nf-enclaveapi-deleteenclave.md). You cannot delete a VBS enclave by calling the [VirtualFree](../memoryapi/nf-memoryapi-virtualfree.md) or [VirtualFreeEx](../memoryapi/nf-memoryapi-virtualfreeex.md) function. You can still delete an SGX enclave by calling **VirtualFree** or **VirtualFreeEx**.

**Windows 10, version 1507, Windows 10, version 1511, Windows 10, version 1607 and Windows 10, version 1703:** To delete the enclave when you finish using it, call the [VirtualFree](../memoryapi/nf-memoryapi-virtualfree.md) or [VirtualFreeEx](../memoryapi/nf-memoryapi-virtualfreeex.md) function and specify the following values:

- The base address of the enclave for the _lpAddress_ parameter.
- 0 for the _dwSize_ parameter.
- **MEM_RELEASE** for the _dwFreeType_ parameter.

## -see-also

[CreateEnclave](nf-enclaveapi-createenclave.md)

[ENCLAVE_INIT_INFO_SGX](../winnt/ns-winnt-enclave_init_info_sgx.md)

[LoadEnclaveData](nf-enclaveapi-loadenclavedata.md)

[VirtualFree](../memoryapi/nf-memoryapi-virtualfree.md)

[VirtualFreeEx](../memoryapi/nf-memoryapi-virtualfreeex.md)
