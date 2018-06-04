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

# IMSVidCtl::get__InputsAvailable


## -description


The <b>get__InputsAvailable</b> method retrieves the input devices that are available in a specified category. 


## -parameters




### -param CategoryGuid [in]

Pointer to a GUID that specifies the category to enumerate. Supported categories include the following.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>KSCATEGORY_BDA_NETWORK_PROVIDER</td>
<td>BDA-compatible tuner devices.</td>
</tr>
<tr>
<td>KSCATEGORY_TVTUNER</td>
<td>Non-BDA analog tuner devices.</td>
</tr>
<tr>
<td>GUID_NULL</td>
<td>Miscellaneous devices (file source, DVD).</td>
</tr>
</table>
 


### -param pVal






#### - ppVal [out]

Receives an <a href="https://msdn.microsoft.com/cb9d9885-718e-43b9-b195-66149bd7e973">IMSVidInputDevices</a> interface pointer. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method returns a read-only collection of input devices. Use the returned <a href="https://msdn.microsoft.com/cb9d9885-718e-43b9-b195-66149bd7e973">IMSVidInputDevices</a> pointer to enumerate the collection.


#### Examples

The following example enumerates the available BDA-compatible tuners and retrieves their friendly names.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
CComPtr&lt;IMSVidInputDevices&gt; pInputs;
hr = pVidControl-&gt;get__InputsAvailable(&amp;KSCATEGORY_BDA_NETWORK_PROVIDER, &amp;pInputs);
if (SUCCEEDED(hr))
{
    long lCount;
    hr = pInputs-&gt;get_Count(&amp;lCount);
    for (long ix = 0; ix &lt; lCount; ix++)
    {
        CComBSTR bstrName;
        CComVariant var(ix);
        CComPtr&lt;IMSVidInputDevice&gt; pInput;
        hr = pInputs-&gt;get_Item(var, &amp;pInput);
        hr = pInput-&gt;get_Name(&amp;bstrName);
        // Display the name.
    }
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/3451002b-5339-4b43-aefd-d66c48f7ae57">IMSVidCtl::get_InputActive</a>
 

 

