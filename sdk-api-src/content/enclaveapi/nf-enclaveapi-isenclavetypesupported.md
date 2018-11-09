---
UID: NF:enclaveapi.IsEnclaveTypeSupported
title: IsEnclaveTypeSupported function
author: windows-sdk-content
description: Retrieves whether the specified type of enclave is supported.
old-location: base\isenclavetypesupported.htm
tech.root: memory
ms.assetid: E46AF02B-324F-43A8-8C73-9FE1E8E771E9
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ENCLAVE_TYPE_SGX, ENCLAVE_TYPE_VBS, IsEnclaveTypeSupported, IsEnclaveTypeSupported function, base.isenclavetypesupported, base.isenclavetypesypported, enclaveapi/IsEnclaveTypeSupported
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
 - IsEnclaveTypeSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

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
</table>
 



