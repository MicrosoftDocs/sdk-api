---
UID: NF:enclaveapi.CreateEnclave
title: CreateEnclave function
author: windows-sdk-content
description: Creates a new uninitialized enclave. An enclave is an isolated region of code and data within the address space for an application. Only code that runs within the enclave can access data within the same enclave.
old-location: base\createenclave.htm
tech.root: Memory
ms.assetid: 2193AE42-D9CC-4A9C-8676-7DE432ED58C3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateEnclave, CreateEnclave function, ENCLAVE_TYPE_SGX, ENCLAVE_TYPE_VBS, base.createenclave, enclaveapi/CreateEnclave
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateEnclave function


## -description


Creates a new uninitialized enclave. An enclave  is an isolated region of code and data within the address space for an application. Only code that runs within the enclave can access data within the same enclave.


## -parameters




### -param hProcess [in]

A handle to the process for which you want to create an enclave.


### -param lpAddress [in, optional]

The preferred base address of the enclave. Specify <b>NULL</b> to have the operating system assign the base address.


### -param dwSize [in]

The size of the enclave that you want to create, including the size of the code that you will load into the enclave, in bytes.


### -param dwInitialCommitment [in]

The amount of memory to commit for the enclave, in bytes.

If the amount of enclave memory available is not sufficient to commit this number of bytes, enclave creation fails. Any memory that remains unused when you initialize the enclave by calling <a href="https://msdn.microsoft.com/6A711135-A522-40AE-965F-E1AF97D0076A">InitializeEnclave</a> is returned to the list of free pages.

The value of the <i>dwInitialCommittment</i> parameter must not exceed the value of the <i>dwSize</i> parameter.

This parameter is not used for virtualization-based security (VBS) enclaves.


### -param flEnclaveType [in]

The architecture type of the enclave that you want to create. To verify that an enclave type is supported, call <a href="https://msdn.microsoft.com/E46AF02B-324F-43A8-8C73-9FE1E8E771E9">IsEnclaveTypeSupported</a>.

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

For the <b>ENCLAVE_TYPE_SGX</b> enclave type, you must specify a pointer to an <a href="https://msdn.microsoft.com/51ED6E75-DA18-4CCE-8718-46328DD62B07">ENCLAVE_CREATE_INFO_SGX</a> structure.

For the <b>ENCLAVE_TYPE_VBS</b> enclave type, you must specify a pointer to an <a href="https://msdn.microsoft.com/5AD6D695-92D6-47AC-A43C-D3A37D28C76C">ENCLAVE_CREATE_INFO_VBS</a> structure.


### -param dwInfoLength [in]

The length of the structure that the <i>lpEnclaveInformation</i> parameter points to, in bytes. For the <b>ENCLAVE_TYPE_SGX</b> enclave type, this value must be 4096.  For the <b>ENCLAVE_TYPE_VBS</b> enclave type, this value must be <code>sizeof(ENCLAVE_CREATE_INFO_VBS)</code>, which is 36 bytes.


### -param lpEnclaveError [out, optional]

An optional pointer to  a variable that receives an enclave error code that is architecture-specific. For the <b>ENCLAVE_TYPE_SGX</b> and <b>ENCLAVE_TYPE_VBS</b>  enclave types, the <i>lpEnclaveError</i> parameter is not used.


## -returns



If the function succeeds, the return value is the base address of the created enclave.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

For a list of common error codes, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>. The following error codes also apply for this function.

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



To load data into an enclave after you create it, call <a href="https://msdn.microsoft.com/CC696026-FB74-4D91-BB40-17610DF41F8F">LoadEnclaveData</a>. To initialize the enclave after you load the data, call <a href="https://msdn.microsoft.com/6A711135-A522-40AE-965F-E1AF97D0076A">InitializeEnclave</a>.

<b>Windows 10, version 1709:  </b>To delete the enclave when you finish using it, call <a href="https://msdn.microsoft.com/04FCD129-3A3B-40EA-AD62-01C674CF2E61">DeleteEnclave</a>. You cannot delete a VBS enclave by calling the <a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a> or <a href="https://msdn.microsoft.com/2e5c862c-1251-49da-9c3a-90b09e488d89">VirtualFreeEx</a> function. You can still delete an SGX enclave by calling <b>VirtualFree</b> or <b>VirtualFreeEx</b>.

<b>Windows 10, version 1507, Windows 10, version 1511, Windows 10, version 1607 and Windows 10, version 1703:  </b>To delete the enclave when you finish using it, call the <a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a> or <a href="https://msdn.microsoft.com/2e5c862c-1251-49da-9c3a-90b09e488d89">VirtualFreeEx</a> function and specify the following values:

<ul>
<li>The base address of the enclave for the <i>lpAddress</i> parameter.</li>
<li>0 for the <i>dwSize</i> parameter.</li>
<li><b>MEM_RELEASE</b> for the <i>dwFreeType</i> parameter. The <b>MEM_DECOMMIT</b> value is not supported for enclaves.</li>
</ul>


For information about the Intel Software Guard Extensions (SGX) architecture extension, see <a href="https://go.microsoft.com/fwlink/p/?linkid=691175">Intel Software Guard Extensions</a>.




## -see-also




<a href="https://msdn.microsoft.com/51ED6E75-DA18-4CCE-8718-46328DD62B07">ENCLAVE_CREATE_INFO_SGX</a>



<a href="https://msdn.microsoft.com/5AD6D695-92D6-47AC-A43C-D3A37D28C76C">ENCLAVE_CREATE_INFO_VBS</a>



<a href="https://msdn.microsoft.com/6A711135-A522-40AE-965F-E1AF97D0076A">InitializeEnclave</a>



<a href="https://msdn.microsoft.com/E46AF02B-324F-43A8-8C73-9FE1E8E771E9">IsEnclaveTypeSupported</a>



<a href="https://msdn.microsoft.com/CC696026-FB74-4D91-BB40-17610DF41F8F">LoadEnclaveData</a>



<a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a>



<a href="https://msdn.microsoft.com/2e5c862c-1251-49da-9c3a-90b09e488d89">VirtualFreeEx</a>
 

 

