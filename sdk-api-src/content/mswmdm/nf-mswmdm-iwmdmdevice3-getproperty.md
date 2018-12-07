---
UID: NF:mswmdm.IWMDMDevice3.GetProperty
title: IWMDMDevice3::GetProperty
author: windows-sdk-content
description: The GetProperty method retrieves a specific device metadata property.
old-location: wmdm\iwmdmdevice3_getproperty.htm
tech.root: WMDM
ms.assetid: f1c8406f-f0cb-4def-bc26-399908ecbf83
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetProperty, GetProperty method [windows Media Device Manager], GetProperty method [windows Media Device Manager],IWMDMDevice3 interface, IWMDMDevice3 interface [windows Media Device Manager],GetProperty method, IWMDMDevice3.GetProperty, IWMDMDevice3::GetProperty, IWMDMDevice3GetProperty, mswmdm/IWMDMDevice3::GetProperty, wmdm.iwmdmdevice3_getproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
req.include-header: 
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDevice3.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMDevice3::GetProperty


## -description



The <b>GetProperty</b> method retrieves a specific device metadata property.




## -parameters




### -param pwszPropName [in]

A wide character, null-terminated string name of the property to retrieve. A list of standard property name constants is given in <a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>.


### -param pValue [out]

Returned value for the property. The application must free this memory using <b>PropVariantClear</b>.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



To obtain the list of supported device properties, the client call this function and specify <b>g_wszWMDMSupportedDeviceProperties</b>. For the list of standard device property names, see <a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>.

The client should pass in a pointer to an empty <b>PROPVARIANT</b> in the <i>pValue</i> parameter. On return, <i>pValue</i> will contain the value of the property.

This method is similar to the <b>GetMetadata</b> and <b>GetSpecifiedMetadata</b> methods for storages, but this method can get only one property at a time.


#### Examples

The following C++ code queries for the g_wszWMDMFormatsSupported property, which returns a <b>SAFEARRAY</b> list of formats supported by a device.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Query a device for supported configurations for each media or format type. 
HRESULT GetCaps(IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Request the "formats supported" property to get a list of supported formats.
    PROPVARIANT pvFormatsSupported;
    PropVariantInit(&amp;pvFormatsSupported);
    hr = pDevice-&gt;GetProperty(g_wszWMDMFormatsSupported, &amp;pvFormatsSupported);
    HANDLE_HR(hr, "Got a property list in GetCaps", "Couldn't get a property list in GetCaps.");

    // Loop through the retrieved format list.
    // For each format, get a list of format configurations.
    SAFEARRAY* formatList = pvFormatsSupported.parray;
    WMDM_FORMATCODE formatCode = WMDM_FORMATCODE_NOTUSED;
    for(LONG iCap = 0; iCap &lt; formatList-&gt;rgsabound[0].cElements; iCap++)
    { 
        // Get a format from the SAFEARRAY of retrieved formats.
        SafeArrayGetElement(formatList, &amp;iCap, &amp;formatCode);

        // Call a custom function to see the specifics of device support for 
       // each format.
        if (formatCode != WMDM_FORMATCODE_NOTUSED)
            myGetFormatCaps(formatCode, pDevice);
    }

e_Exit:
    // Clear out the memory we used.
    PropVariantClear(&amp;pvFormatsSupported);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c5935681-b530-4446-a026-7ddc74084d23">Enumerating Devices</a>



<a href="https://msdn.microsoft.com/29e0ec95-c1ea-4157-b5aa-39d80fff407d">IWMDMDevice3 Interface</a>



<a href="https://msdn.microsoft.com/39483d9a-0725-45fa-9d41-dbabd400b3bf">IWMDMDevice3::SetProperty</a>



<a href="https://msdn.microsoft.com/7e436742-fb19-4e8e-98a2-d961c9f0ecbf">IWMDMStorage3::GetMetadata</a>



<a href="https://msdn.microsoft.com/c4e2c889-9ad0-42d1-bb50-4ebcb9859715">IWMDMStorage4::GetSpecifiedMetadata</a>



<a href="https://msdn.microsoft.com/478a5412-e8b4-41c8-802f-9c2748dbaeae">Setting Metadata on a File</a>
 

 

