---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RoResolveRestrictedErrorInfoReference function


## -description


Returns the <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> interface pointer based on the given reference.


## -parameters




### -param reference [in]

Type: <b>PCWSTR</b>

Identifies an error object which contains relevant information for the specific error.


### -param ppRestrictedErrorInfo [out]

Type: <b><a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a>**</b>

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



The <b>RoResolveRestrictedErrorInfoReference</b> function is useful primarily for debugger development. A debugger receives the reference  string and uses the reference to identify the associated <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> object, which allows the debugger to retrieve the detailed error message by calling the <a href="https://msdn.microsoft.com/ecfd97cf-9f8f-4940-9499-a894e0883f04">GetErrorDetails</a> method.




#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT DebuggerIntegration(PCWST   referenceName)
{
    HRESULT hr = S_OK;
    IRestrictedErrorInfo *pRORestrictedErrorInfo = nullptr;

    // Resove the IRestrictedErrorInfo
    hr = RoResolveRestrictedErrorInfoReference(referenceName,  
                      reinterpret_cast&lt;void**&gt;(&amp;pRORestrictedErrorInfo));
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
        hr = spRestrictedErrorInfo-&gt;GetErrorDetails(&amp;bstrDescription, 
                                      &amp;hrError, &amp;bstrRestrictedDescription);
        if (FAILED(hr))
        {
            hr = E_FAIL;    
        }
    }

   return hr;

}
</pre>
</td>
</tr>
</table></span></div>


