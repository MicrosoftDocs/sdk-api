---
UID: NF:enclaveapi.IsEnclaveTypeSupported
title: IsEnclaveTypeSupported function (enclaveapi.h)
author: windows-sdk-content
description: Retrieves whether the specified type of enclave is supported.
old-location: base\isenclavetypesupported.htm
tech.root: Memory
ms.assetid: E46AF02B-324F-43A8-8C73-9FE1E8E771E9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ENCLAVE_TYPE_SGX, ENCLAVE_TYPE_VBS, IsEnclaveTypeSupported, IsEnclaveTypeSupported function, base.isenclavetypesupported, base.isenclavetypesypported, enclaveapi/IsEnclaveTypeSupported
ms.topic: function
f1_keywords: 
 - "enclaveapi/IsEnclaveTypeSupported"
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
 - IsEnclaveTypeSupported
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsEnclaveTypeSupported function


## -description


Retrieves whether the specified type of enclave is supported.


## -parameters




### -param flEnclaveType [in]

The type of enclave to check.

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
A  virtualization-based security (VBS) enclave.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>. The following error codes also apply for this function.

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
</table>
 



