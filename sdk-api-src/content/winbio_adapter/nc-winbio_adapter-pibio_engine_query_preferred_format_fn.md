---
UID: NC:winbio_adapter.PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN
title: PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN (winbio_adapter.h)
description: Determines the input data format preferred by the engine adapter.
helpviewer_keywords: ["EngineAdapterQueryPreferredFormat","EngineAdapterQueryPreferredFormat callback function [Windows Biometric Framework API]","PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN","PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN callback","secbiomet.engineadapterquerypreferredformat","winbio_adapter/EngineAdapterQueryPreferredFormat"]
old-location: secbiomet\engineadapterquerypreferredformat.htm
tech.root: SecBioMet
ms.assetid: df76e7d7-9a71-4c98-b038-8925d8cf0980
ms.date: 12/05/2018
ms.keywords: EngineAdapterQueryPreferredFormat, EngineAdapterQueryPreferredFormat callback function [Windows Biometric Framework API], PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN, PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN callback, secbiomet.engineadapterquerypreferredformat, winbio_adapter/EngineAdapterQueryPreferredFormat
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN
 - winbio_adapter/PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterQueryPreferredFormat
---

# PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN callback function


## -description

Called by the sensor adapter on the biometric unit to determine the input data format preferred by the  engine adapter.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param StandardFormat [out]

Pointer to a <a href="/windows/desktop/SecBioMet/winbio-registered-format">WINBIO_REGISTERED_FORMAT</a> structure that specifies the format of the data in the <b>StandardDataBlock</b> member of the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> object. The format is an IBIA-registered name/value pair.

### -param VendorFormat [out]

Pointer to a GUID that receives the vendor-defined format of the data in the <b>VendorDataBlock</b> member of the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> object.

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


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
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
   StandardFormat->Owner = WINBIO_ANSI_381_FORMAT_OWNER;
   StandardFormat->Type = WINBIO_ANSI_381_FORMAT_TYPE;
   *VendorFormat = VENDOR_UUID_VALUE;

cleanup:

    return hr;
}
```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>