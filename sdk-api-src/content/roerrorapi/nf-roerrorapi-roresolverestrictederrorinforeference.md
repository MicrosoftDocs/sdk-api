---
UID: NF:roerrorapi.RoResolveRestrictedErrorInfoReference
title: RoResolveRestrictedErrorInfoReference function
description: Returns the IRestrictedErrorInfo interface pointer based on the given reference.
helpviewer_keywords: ["RoResolveRestrictedErrorInfoReference","RoResolveRestrictedErrorInfoReference function [Windows Runtime]","roerrorapi/RoResolveRestrictedErrorInfoReference","winrt.roresolverestrictederrorinforeference"]
old-location: winrt\roresolverestrictederrorinforeference.htm
tech.root: WinRT
ms.assetid: 2F5C5A84-502C-4BD1-A01F-8F0E9B5857AD
ms.date: 12/5/2018
ms.keywords: RoResolveRestrictedErrorInfoReference, RoResolveRestrictedErrorInfoReference function [Windows Runtime], roerrorapi/RoResolveRestrictedErrorInfoReference, winrt.roresolverestrictederrorinforeference
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Runtimeobject.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - RoResolveRestrictedErrorInfoReference
 - roerrorapi/RoResolveRestrictedErrorInfoReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - runtimeobject.lib
 - runtimeobject.dll
 - API-MS-Win-Core-WinRT-error-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - RoResolveRestrictedErrorInfoReference
---

# RoResolveRestrictedErrorInfoReference function


## -description

Returns the <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> interface pointer based on the given reference.

## -parameters

### -param reference [in]

Type: <b>PCWSTR</b>

Identifies an error object which contains relevant information for the specific error.

### -param ppRestrictedErrorInfo [out]

Type: <b><a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a>**</b>

The output parameter for the object associated with the given reference.

## -returns

Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLASS_E_NOAGGREGATION</b></dt>
</dl>
</td>
<td width="60%">
object does not support aggregation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The reference is invalid.



</td>
</tr>
</table>

## -remarks

The <b>RoResolveRestrictedErrorInfoReference</b> function is useful primarily for debugger development. A debugger receives the reference  string and uses the reference to identify the associated <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> object, which allows the debugger to retrieve the detailed error message by calling the <a href="/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-irestrictederrorinfo-geterrordetails">GetErrorDetails</a> method.




#### Examples

```cpp
HRESULT DebuggerIntegration(PCWST   referenceName)
{
    HRESULT hr = S_OK;
    IRestrictedErrorInfo *pRORestrictedErrorInfo = nullptr;

    // Resolve the IRestrictedErrorInfo
    hr = RoResolveRestrictedErrorInfoReference(referenceName,  
                      reinterpret_cast<void**>(&pRORestrictedErrorInfo));
    if (FAILED(hr))
    {
        hr = E_FAIL;
    }


    HRESULT hrError = S_OK;
    BSTR bstrDescription = nullptr;
    BSTR bstrRestrictedDescription = nullptr;

    // Get the error details out of the interface
    if (SUCCEEDED(hr))
    {
        hr = spRestrictedErrorInfo->GetErrorDetails(&bstrDescription,
                                      &hrError, &bstrRestrictedDescription);
        if (FAILED(hr))
        {
            hr = E_FAIL;
        }
    }

   return hr;

}
```