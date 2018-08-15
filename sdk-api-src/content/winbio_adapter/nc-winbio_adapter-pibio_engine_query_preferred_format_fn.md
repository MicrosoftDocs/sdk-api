---
UID: NC:winbio_adapter.PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN
title: PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN
author: windows-sdk-content
description: Determines the input data format preferred by the engine adapter.
old-location: secbiomet\engineadapterquerypreferredformat.htm
old-project: secbiomet
ms.assetid: df76e7d7-9a71-4c98-b038-8925d8cf0980
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: EngineAdapterQueryPreferredFormat, EngineAdapterQueryPreferredFormat callback function [Windows Biometric Framework API], PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN, PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN callback, secbiomet.engineadapterquerypreferredformat, winbio_adapter/EngineAdapterQueryPreferredFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.redist: 
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
tech.root: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterQueryPreferredFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN callback function


## -description


Called by the sensor adapter on the biometric unit to determine the input data format preferred by the  engine adapter.


## -parameters




### -param Pipeline [in, out]

Pointer to a <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param StandardFormat [out]

Pointer to a <a href="https://msdn.microsoft.com/a178840e-81cc-4dd3-9d80-a181fa7fa888">WINBIO_REGISTERED_FORMAT</a> structure that specifies the format of the data in the <b>StandardDataBlock</b> member of the <a href="https://msdn.microsoft.com/39cfab34-0416-4897-bf95-a1b3c3a6a7a1">WINBIO_BIR</a> object. The format is an IBIA-registered name/value pair.


### -param VendorFormat [out]

Pointer to a GUID that receives the vendor-defined format of the data in the <b>VendorDataBlock</b> member of the <a href="https://msdn.microsoft.com/39cfab34-0416-4897-bf95-a1b3c3a6a7a1">WINBIO_BIR</a> object.


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
</table>
 




## -remarks



The sensor adapter calls this function to determine the biometric capture format.


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
// EngineAdapterQueryPreferredFormat
//
// Purpose:
//      Called by the sensor adapter on the biometric unit to determine the 
//      input data format preferred by the engine adapter.
//
// Parameters:
//      Pipeline        - Pointer to a WINBIO_PIPELINE structure associated 
//                        with the biometric unit performing the operation.
//      StandardFormat  - Pointer to a WINBIO_REGISTERED_FORMAT structure 
//                        that specifies the format of the data in the 
//                        StandardDataBlock member of the WINBIO_BIR object. 
//                        The format is an IBIA-registered name/value pair.
//      VendorFormat    - Pointer to a GUID that receives the vendor-defined 
//                        format of the data in the VendorDataBlock member of 
//                        the WINBIO_BIR object.
//
static HRESULT
WINAPI
EngineAdapterQueryPreferredFormat(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_REGISTERED_FORMAT StandardFormat,
    __out PWINBIO_UUID VendorFormat
    )
{
   HRESULT hr = S_OK;

   // Verify that pointer arguments are not NULL.
   if (!ARGUMENT_PRESENT(Pipeline) ||
       !ARGUMENT_PRESENT(StandardFormat) ||
       !ARGUMENT_PRESENT(VendorFormat))
   {
        hr = E_POINTER;
        goto cleanup;
   }

   // Specify the preferred data formats.
   StandardFormat-&gt;Owner = WINBIO_ANSI_381_FORMAT_OWNER;
   StandardFormat-&gt;Type = WINBIO_ANSI_381_FORMAT_TYPE;
   *VendorFormat = VENDOR_UUID_VALUE;

cleanup:

    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

