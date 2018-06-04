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

# IWMDMDevice2::GetCanonicalName


## -description



The <b>GetCanonicalName</b> method retrieves the canonical name of the device.




## -parameters




### -param pwszPnPName [out]

Wide-character buffer for the canonical names. This buffer must be allocated and released by the caller.


### -param nMaxChars [in]

Integer specifying the maximum number of characters that can be placed in <i>pwszPnPName</i>, including the termination character.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszPnPName</i> parameter is an invalid or <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The device does not support a canonical name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified is too small for the canonical name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



The application can use the retrieved canonical name to call <a href="https://msdn.microsoft.com/cfa0fe8d-668a-443b-be50-cf1f83362a14">IWMDeviceManager2::GetDeviceFromCanonicalName</a> to find this device again.

The returned canonical name is in the format &lt; <i>PnP Device Path</i> &gt;$&lt; <i>index</i> &gt;, where <i>index</i> is a zero-based index into the device objects returned by the service provider for the specified PnP device path.

The format of canonical name is subject to change in future releases of Windows Media Device Manager.


#### Examples

The following C++ code retrieves a device canonical name.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Obtain an IWMDMDevice2 interface and call
// some methods.
const UINT MAX_CHARS = 100;
CComQIPtr&lt;IWMDMDevice2&gt; pIWMDMDevice2(pIWMDMDevice);
if (pIWMDMDevice2 != NULL)
{
    // Get the canonical name.
    WCHAR canonicalName[MAX_CHARS];
    hr = pIWMDMDevice2-&gt;GetCanonicalName(canonicalName, MAX_CHARS);
    if (hr == S_OK)
    {
        // TODO: Retrieve the canonical name.
    }

    // Find out the driver.
    myGetDriverName(pIWMDMDevice2);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9">IWMDMDevice2 Interface</a>



<a href="https://msdn.microsoft.com/cfa0fe8d-668a-443b-be50-cf1f83362a14">IWMDeviceManager2::GetDeviceFromCanonicalName</a>
 

 

