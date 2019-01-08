---
UID: NC:ntsecpkg.SpQueryContextAttributesFn
title: SpQueryContextAttributesFn
author: windows-sdk-content
description: Retrieves the attributes of a security context.
old-location: security\spquerycontextattributes.htm
tech.root: SecAuthN
ms.assetid: 720b37dd-a957-4da9-8b94-4642e515bc22
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SpQueryContextAttributes, SpQueryContextAttributes callback function [Security], SpQueryContextAttributesFn, SpQueryContextAttributesFn callback, _ssp_spquerycontextattributes, ntsecpkg/SpQueryContextAttributes, security.spquerycontextattributes
ms.topic: callback
req.header: ntsecpkg.h
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
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpQueryContextAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SpQueryContextAttributesFn callback function


## -description


The <b>SpQueryContextAttributes</b> function retrieves the attributes of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.

The <b>SpQueryContextAttributes</b> function is the dispatch function for the 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function of the 
<a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">Security Support Provider Interface</a>.


## -parameters




### -param ContextHandle [in]

A handle to the security context.


### -param ContextAttribute [in]

Context attribute to query. For a list of valid values, see the 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function.


### -param Buffer [out]

Pointer that receives the address of a buffer containing the requested attributes. Memory for the <i>Buffer</i> parameter should be allocated with the 
<a href="https://msdn.microsoft.com/8e97ea0e-42f5-4641-83d7-3858c533479c">AllocateHeap</a> function from the 
<a href="https://msdn.microsoft.com/a7881f06-792c-4791-9aa6-9a7eb202020b">SECPKG_DLL_FUNCTIONS</a> function table in user-mode. In <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) mode, use the 
<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateLsaHeap</a> function.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following  lists a common reason for failure and the error code that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>
 




## -remarks



SSP/APs must implement the <b>SpQueryContextAttributes</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the LSA-mode implementation of the <b>SpQueryContextAttributes</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.

A pointer to the user-mode implementation of the <b>SpQueryContextAttributes</b> function is available in the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

