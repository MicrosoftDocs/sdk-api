---
UID: NF:enclaveapi.CreateEnclave
title: CreateEnclave function (enclaveapi.h)
description: Creates a new uninitialized enclave. An enclave is an isolated region of code and data within the address space for an application. Only code that runs within the enclave can access data within the same enclave.
helpviewer_keywords: ["CreateEnclave","CreateEnclave function","ENCLAVE_TYPE_SGX","ENCLAVE_TYPE_SGX2","ENCLAVE_TYPE_VBS","base.createenclave","enclaveapi/CreateEnclave"]
old-location: base\createenclave.htm
tech.root: base
ms.assetid: 2193AE42-D9CC-4A9C-8676-7DE432ED58C3
ms.date: 05/06/2022
ms.keywords: CreateEnclave, CreateEnclave function, ENCLAVE_TYPE_SGX, ENCLAVE_TYPE_SGX2, ENCLAVE_TYPE_VBS, base.createenclave, enclaveapi/CreateEnclave
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
 - CreateEnclave
 - enclaveapi/CreateEnclave
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
 - CreateEnclave
---

# CreateEnclave function

## -description

Creates a new uninitialized enclave. An enclave  is an isolated region of code and data within the address space for an application. Only code that runs within the enclave can access data within the same enclave.

## -parameters

### -param hProcess [in]

A handle to the process for which you want to create an enclave.

### -param lpAddress [in, optional]

The preferred base address of the enclave. Specify **NULL** to have the operating system assign the base address.

### -param dwSize [in]

The size of the enclave that you want to create, including the size of the code that you will load into the enclave, in bytes.

VBS enclaves must be a multiple of 2 MB in size.

SGX enclaves must be a power of 2 in size and must have their base aligned to the same power of 2 as the size, with a minimum alignment of 2 MB. As an example, if the enclave is 128 MB, then its base must be aligned to a 128 MB boundary.

### -param dwInitialCommitment [in]

The amount of memory to commit for the enclave, in bytes.

If the amount of enclave memory available is not sufficient to commit this number of bytes, enclave creation fails. Any memory that remains unused when you initialize the enclave by calling <a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave">InitializeEnclave</a> is returned to the list of free pages.

The value of the <i>dwInitialCommittment</i> parameter must not exceed the value of the <i>dwSize</i> parameter.

This parameter is not used for virtualization-based security (VBS) enclaves.

### -param flEnclaveType [in]

The architecture type of the enclave that you want to create. To verify that an enclave type is supported, call <a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported">IsEnclaveTypeSupported</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_TYPE_SGX"></a><a id="enclave_type_sgx"></a><dl>
<dt><b><b>ENCLAVE_TYPE_SGX</b></b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
An enclave for the Intel Software Guard Extensions (SGX) architecture extension.

</td>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_TYPE_SGX2"></a><a id="enclave_type_sgx2"></a><dl>
<dt><b><b>ENCLAVE_TYPE_SGX2</b></b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Supports SGX2 and SGX1 enclaves. The platform and OS support SGX2 instructions with EDMM on this platform (in addition to other SGX2 constructs).

</td>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_TYPE_VBS"></a><a id="enclave_type_vbs"></a><dl>
<dt><b>ENCLAVE_TYPE_VBS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
A  VBS enclave.

</td>
</tr>
</table>

### -param lpEnclaveInformation [in]

A pointer to the architecture-specific information to use to create the enclave.

For the **ENCLAVE_TYPE_SGX** and **ENCLAVE_TYPE_SGX2** enclave types, you must specify a pointer to an [ENCLAVE_CREATE_INFO_SGX](/windows/win32/api/winnt/ns-winnt-enclave_create_info_sgx) structure.

For the **ENCLAVE_TYPE_VBS** enclave type, you must specify a pointer to an [ENCLAVE_CREATE_INFO_VBS](/windows/win32/api/winnt/ns-winnt-enclave_create_info_vbs) structure.

### -param dwInfoLength [in]

The length of the structure that the _lpEnclaveInformation_ parameter points to, in bytes. For the **ENCLAVE_TYPE_SGX** and **ENCLAVE_TYPE_SGX2** enclave types, this value must be 4096.  For the **ENCLAVE_TYPE_VBS** enclave type, this value must be `sizeof(ENCLAVE_CREATE_INFO_VBS)`, which is 36 bytes.

### -param lpEnclaveError [out, optional]

An optional pointer to  a variable that receives an enclave error code that is architecture-specific. For the **ENCLAVE_TYPE_SGX**, **ENCLAVE_TYPE_SGX2** and **ENCLAVE_TYPE_VBS**  enclave types, the _lpEnclaveError_ parameter is not used.

## -returns

If the function succeeds, the return value is the base address of the created enclave.

If the function fails, the return value is **NULL**. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

For a list of common error codes, see [System Error Codes](/windows/win32/Debug/system-error-codes). The following error codes also apply for this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_NOT_SUPPORTED</b></b></dt>
</dl>
</td>
<td width="60%">
An unsupported enclave type was specified.

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
</table>

## -remarks

To load data into an enclave after you create it, call <a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata">LoadEnclaveData</a>. To initialize the enclave after you load the data, call <a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave">InitializeEnclave</a>.

<b>Windows 10, version 1709:  </b>To delete the enclave when you finish using it, call <a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-deleteenclave">DeleteEnclave</a>. You cannot delete a VBS enclave by calling the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a> or <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfreeex">VirtualFreeEx</a> function. You can still delete an SGX enclave by calling <b>VirtualFree</b> or <b>VirtualFreeEx</b>.

<b>Windows 10, version 1507, Windows 10, version 1511, Windows 10, version 1607 and Windows 10, version 1703:  </b>To delete the enclave when you finish using it, call the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a> or <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfreeex">VirtualFreeEx</a> function and specify the following values:

<ul>
<li>The base address of the enclave for the <i>lpAddress</i> parameter.</li>
<li>0 for the <i>dwSize</i> parameter.</li>
<li><b>MEM_RELEASE</b> for the <i>dwFreeType</i> parameter. The <b>MEM_DECOMMIT</b> value is not supported for enclaves.</li>
</ul>


For information about the Intel Software Guard Extensions (SGX) architecture extension, see <a href="https://software.intel.com/sgx">Intel Software Guard Extensions</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx">ENCLAVE_CREATE_INFO_SGX</a>



<a href="/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs">ENCLAVE_CREATE_INFO_VBS</a>



<a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave">InitializeEnclave</a>



<a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported">IsEnclaveTypeSupported</a>



<a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata">LoadEnclaveData</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfreeex">VirtualFreeEx</a>
