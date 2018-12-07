---
UID: NF:msvidctl.IMSVidCtl.get__InputsAvailable
title: IMSVidCtl::get__InputsAvailable
author: windows-sdk-content
description: The get__InputsAvailable method retrieves the input devices that are available in a specified category.
old-location: mstv\imsvidctl_get__inputsavailable.htm
tech.root: mstv
ms.assetid: 2d77eca3-aec9-423d-8d02-92e6f9ab5167
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get__InputsAvailable method, IMSVidCtl.get__InputsAvailable, IMSVidCtl::get__InputsAvailable, IMSVidCtlget__InputsAvailable, get__InputsAvailable, get__InputsAvailable method [Microsoft TV Technologies], get__InputsAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get__inputsavailable, msvidctl/IMSVidCtl::get__InputsAvailable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get__InputsAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::get__InputsAvailable


## -description


The <b>get__InputsAvailable</b> method retrieves the input devices that are available in a specified category. 


## -parameters




### -param CategoryGuid [in]

Pointer to a GUID that specifies the category to enumerate. Supported categories include the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
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
 


### -param pVal [out]

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
 

 

