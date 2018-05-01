---
UID: NC:winbio_adapter.PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN
title: PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN
author: windows-driver-content
description: Retrieves an array of object identifiers that represent the hash algorithms supported by the engine adapter.
old-location: secbiomet\engineadapterqueryhashalgorithms.htm
old-project: SecBioMet
ms.assetid: 66766c80-44b5-4bec-b8cc-32adf1ddae8a
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: EngineAdapterQueryHashAlgorithms, EngineAdapterQueryHashAlgorithms callback function [Windows Biometric Framework API], PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN, secbiomet.engineadapterqueryhashalgorithms, winbio_adapter/EngineAdapterQueryHashAlgorithms
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio_adapter.h
api_name:
-	EngineAdapterQueryHashAlgorithms
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN callback


## -description


Called by the Windows Biometric Framework to retrieve an array of  object identifiers (OIDs) that represent the hash algorithms supported by the engine adapter.


## -parameters




### -param Pipeline [in, out]

Pointer to a <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param AlgorithmCount [out]

Pointer to a value that receives the number of algorithm OID strings in the buffer specified by the <i>AlgorithmBuffer</i> parameter.



### -param AlgorithmBufferSize [out]

Pointer to a value that contains the size, in bytes, of the buffer specified by the <i>AlgorithmBuffer</i> parameter. The size includes the two <b>NULL</b> values that terminate the buffer.


### -param *AlgorithmBuffer [out]

Address of a variable that receives a pointer to a buffer that contains packed, <b>NULL</b>-terminated ANSI strings. Each string represents an OID for a hash algorithm. The final string in the buffer must be terminated by two successive <b>NULL</b> values.


## -returns



If the function succeeds, it returns S_OK. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A mandatory pointer parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The engine adapter does not support template hash generation.

</td>
</tr>
</table>
 




## -remarks



Only the SHA1 hash algorithm is used by the Windows Biometric Framework. Therefore, this OID must be included in the buffer. Other OID strings are optional and can be included for future Windows versions. In Wincrypt.h, included with the Windows SDK, the symbol for the SHA1 algorithm is szOID_OIWSEC_sha1 and the associated string value is "1.3.14.3.2.26". This string value must be in the buffer. See Wincrypt.h for other OID values.

The following example shows how to create an OID buffer. The SHA1 algorithm ("1.3.14.3.2.26") is included first although the order of inclusion is not important. Another algorithm, szOID_OIWSEC_shaRSA with a value of "1.3.14.3.2.15" is also included. Note that a single <b>NULL</b> value identifies the end of each OID string and that an additional <b>NULL</b> value after the end of the last string identifies the end of the buffer. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>char OidBuffer[] = 
{
    '1','.','3','.','1','4','.','3','.','2','.','2','6','\0',
    '1','.','3','.','1','4','.','3','.','2','.','1','5','\0','\0'
};
</pre>
</td>
</tr>
</table></span></div>
If this function succeeds, return the address of the start of this buffer in the <i>AlgorithmBuffer</i> argument. The engine adapter owns the buffer. Because the Windows Biometric Framework reads the buffer, the address must remain valid as long as the engine adapter is attached to the biometric unit.

Typically, you compile the table of OID strings into the engine adapter as a static data block.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterQueryHashAlgorithms
// 
//      Retrieves an array of object identifiers (OIDs) that represent the 
//      hash algorithms supported by the engine adapter.
//
// Parameters:
//      Pipeline            - Pointer to a WINBIO_PIPELINE structure associated 
//                            with the biometric unit performing the operation.
//      AlgorithmCount      - Pointer to a value that receives the number of 
//                            algorithm OID strings specified by the 
//                            AlgorithmBuffer parameter.
//      AlgorithmBufferSize - Pointer to a value that contains the size, 
//                            in bytes, of the buffer specified by the 
//                            AlgorithmBuffer parameter.
//      AlgorithmBuffer     - Address of a variable that receives a pointer to 
//                            a buffer that contains packed, NULL-terminated ANSI 
//                            strings. Each string represents an OID for a hash 
//                            algorithm. The final string in the buffer must be 
//                            terminated by two successive NULL values.
//
// Note:
//      The following algorithm table contains the SHA1 OID. Only 
//      the SHA1 hash algorithm is supported by the Windows Biometric Framework.
//      The algorithm table must be defined in global scope for the engine adapter.
//

static char g_HashAlgorithmOidTable[] = 
{
    '1','.','3','.','1','4','.','3','.','2','.','2','6','\0','\0'
};

static HRESULT
WINAPI
EngineAdapterQueryHashAlgorithms(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PSIZE_T AlgorithmCount,
    __out PSIZE_T AlgorithmBufferSize,
    __out PUCHAR *AlgorithmBuffer
    )
{
    ////////////////////////////////////////////////////////////////////////////
    // Return E_NOTIMPL here if your adapter does not support template hashing.
    ////////////////////////////////////////////////////////////////////////////

    HRESULT hr = S_OK;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(AlgorithmCount) ||
        !ARGUMENT_PRESENT(AlgorithmBufferSize) ||
        !ARGUMENT_PRESENT(AlgorithmBuffer))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Pass the address and size of the static algorithm table and the number
    // of algorithms to the caller. If your adapter does not support template
    // hashing, return E_NOTIMPL.
    *AlgorithmCount = 1;
    *AlgorithmBufferSize = sizeof(g_HashAlgorithmOidTable);
    *AlgorithmBuffer = g_HashAlgorithmOidTable;

cleanup:

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0d16d82a-287c-4402-ac10-f601684bd976">EngineAdapterSetHashAlgorithm</a>



<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

