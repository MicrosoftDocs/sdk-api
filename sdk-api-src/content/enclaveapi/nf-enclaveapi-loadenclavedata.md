---
UID: NF:enclaveapi.LoadEnclaveData
title: LoadEnclaveData function
author: windows-sdk-content
description: Loads data into an uninitialized enclave that you created by calling CreateEnclave.
old-location: base\loadenclavedata.htm
old-project: memory
ms.assetid: CC696026-FB74-4D91-BB40-17610DF41F8F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LoadEnclaveData, LoadEnclaveData function, base.loadenclavedata, enclaveapi/LoadEnclaveData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: enclaveapi.h
req.include-header: Winbase.h
req.redist: 
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
tech.root: 
req.typenames: ProtType
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
 - LoadEnclaveData
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Api-ms-win-core-enclave-l1-1-0.dll; Kernel32.dll; KernelBase.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# LoadEnclaveData function


## -description


Loads data into an  uninitialized enclave that you created by calling <a href="https://msdn.microsoft.com/2193AE42-D9CC-4A9C-8676-7DE432ED58C3">CreateEnclave</a>.


## -parameters




### -param hProcess [in]

A handle to the process for which the enclave was created.


### -param lpAddress [in]

The address in the enclave where you want to load the data.


### -param lpBuffer [in]

A pointer to the data the you want to load into the enclave.


### -param nSize [in]

The size of the data that you want to load into the enclave, in bytes. This value must be a whole-number multiple of the page size.


### -param flProtect [in]

The memory protection to use for the pages that you want to add to the enclave. For a list of memory protection values, see <a href="https://msdn.microsoft.com/09839db7-2118-4a7d-a707-a08c92bd600c">memory protection constants</a>. This value must not include the following constants:

<ul>
<li><b>PAGE_GUARD</b></li>
<li><b>PAGE_NOCACHE</b></li>
<li><b>PAGE_WRITECOMBINE</b></li>
<li><b>PAGE_NOACCESS</b></li>
</ul>
This value can include the enclave specific constants that the following table describes.

<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td><b>PAGE_ENCLAVE_THREAD_CONTROL</b></td>
<td>The page contains a thread control structure (TCS).</td>
</tr>
<tr>
<td><b>PAGE_ENCLAVE_UNVALIDATED</b></td>
<td>The page contents that you supply are excluded from measurement with the EEXTEND instruction of the Intel Software Guard Extensions programming model.</td>
</tr>
</table>
 


### -param lpPageInformation [in]

		A pointer to information that describes the pages that you want to add to the enclave. The <i>lpPageInformation</i> parameter is not used.


### -param dwInfoLength [in]

The length of the structure that the <i>lpPageInformation</i> parameter points to, in bytes. This value must be 0.


### -param lpNumberOfBytesWritten [out]

A pointer to a variable that receives the number of bytes that <b>LoadEnclaveData</b> copied into the enclave.


### -param lpEnclaveError [out, optional]

An optional pointer to  a variable that receives an enclave error code that is architecture-specific. The <i>lpEnclaveError</i> parameter is not used.


## -returns



If all of the data is loaded into the enclave successfully, the return value is nonzero. Otherwise, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

For a list of common error codes, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>. The following error codes also apply for this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_BAD_LENGTH</b></b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>dwInfoLength</i> parameter did not match the value expected based on the value specified for the <i>lpPageInformation</i> parameter.

</td>
</tr>
</table>
 




## -remarks



To initialize the enclave after you load data into the enclave, call <a href="https://msdn.microsoft.com/6A711135-A522-40AE-965F-E1AF97D0076A">InitializeEnclave</a>.

<b>LoadEnclaveData</b> is only supported enclaves that have  the <b>ENCLAVE_TYPE_SGX</b> enclave type.




## -see-also




<a href="https://msdn.microsoft.com/2193AE42-D9CC-4A9C-8676-7DE432ED58C3">CreateEnclave</a>



<a href="https://msdn.microsoft.com/6A711135-A522-40AE-965F-E1AF97D0076A">InitializeEnclave</a>
 

 

