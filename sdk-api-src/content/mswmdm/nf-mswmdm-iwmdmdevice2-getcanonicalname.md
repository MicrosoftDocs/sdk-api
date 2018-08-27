---
UID: NF:mswmdm.IWMDMDevice2.GetCanonicalName
title: IWMDMDevice2::GetCanonicalName
author: windows-sdk-content
description: The GetCanonicalName method retrieves the canonical name of the device.
old-location: wmdm\iwmdmdevice2_getcanonicalname.htm
old-project: WMDM
ms.assetid: 16e18a9e-315f-41a2-b895-e3e478720864
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCanonicalName, GetCanonicalName method [windows Media Device Manager], GetCanonicalName method [windows Media Device Manager],IWMDMDevice2 interface, IWMDMDevice2 interface [windows Media Device Manager],GetCanonicalName method, IWMDMDevice2.GetCanonicalName, IWMDMDevice2::GetCanonicalName, IWMDMDevice2GetPnPName, mswmdm/IWMDMDevice2::GetCanonicalName, wmdm.iwmdmdevice2_getcanonicalname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDevice2.GetCanonicalName
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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


```cpp

// Obtain an IWMDMDevice2 interface and call
// some methods.
const UINT MAX_CHARS = 100;
CComQIPtr<IWMDMDevice2> pIWMDMDevice2(pIWMDMDevice);
if (pIWMDMDevice2 != NULL)
{
    // Get the canonical name.
    WCHAR canonicalName[MAX_CHARS];
    hr = pIWMDMDevice2->GetCanonicalName(canonicalName, MAX_CHARS);
    if (hr == S_OK)
    {
        // TODO: Retrieve the canonical name.
    }

    // Find out the driver.
    myGetDriverName(pIWMDMDevice2);
}

```





## -see-also




<a href="https://msdn.microsoft.com/d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9">IWMDMDevice2 Interface</a>



<a href="https://msdn.microsoft.com/cfa0fe8d-668a-443b-be50-cf1f83362a14">IWMDeviceManager2::GetDeviceFromCanonicalName</a>
 

 

