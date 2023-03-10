---
UID: NF:mswmdm.IWMDMDevice3.GetProperty
title: IWMDMDevice3::GetProperty (mswmdm.h)
description: The GetProperty method retrieves a specific device metadata property.
helpviewer_keywords: ["GetProperty","GetProperty method [windows Media Device Manager]","GetProperty method [windows Media Device Manager]","IWMDMDevice3 interface","IWMDMDevice3 interface [windows Media Device Manager]","GetProperty method","IWMDMDevice3.GetProperty","IWMDMDevice3::GetProperty","IWMDMDevice3GetProperty","mswmdm/IWMDMDevice3::GetProperty","wmdm.iwmdmdevice3_getproperty"]
old-location: wmdm\iwmdmdevice3_getproperty.htm
tech.root: WMDM
ms.assetid: f1c8406f-f0cb-4def-bc26-399908ecbf83
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [windows Media Device Manager], GetProperty method [windows Media Device Manager],IWMDMDevice3 interface, IWMDMDevice3 interface [windows Media Device Manager],GetProperty method, IWMDMDevice3.GetProperty, IWMDMDevice3::GetProperty, IWMDMDevice3GetProperty, mswmdm/IWMDMDevice3::GetProperty, wmdm.iwmdmdevice3_getproperty
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMDevice3::GetProperty
 - mswmdm/IWMDMDevice3::GetProperty
dev_langs:
 - c++
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
---

# IWMDMDevice3::GetProperty


## -description

The <b>GetProperty</b> method retrieves a specific device metadata property.

## -parameters

### -param pwszPropName [in]

A wide character, null-terminated string name of the property to retrieve. A list of standard property name constants is given in <a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>.

### -param pValue [out]

Returned value for the property. The application must free this memory using <b>PropVariantClear</b>.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

To obtain the list of supported device properties, the client call this function and specify <b>g_wszWMDMSupportedDeviceProperties</b>. For the list of standard device property names, see <a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>.

The client should pass in a pointer to an empty <b>PROPVARIANT</b> in the <i>pValue</i> parameter. On return, <i>pValue</i> will contain the value of the property.

This method is similar to the <b>GetMetadata</b> and <b>GetSpecifiedMetadata</b> methods for storages, but this method can get only one property at a time.


#### Examples

The following C++ code queries for the g_wszWMDMFormatsSupported property, which returns a <b>SAFEARRAY</b> list of formats supported by a device.


```cpp

// Query a device for supported configurations for each media or format type. 
HRESULT GetCaps(IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Request the "formats supported" property to get a list of supported formats.
    PROPVARIANT pvFormatsSupported;
    PropVariantInit(&pvFormatsSupported);
    hr = pDevice->GetProperty(g_wszWMDMFormatsSupported, &pvFormatsSupported);
    HANDLE_HR(hr, "Got a property list in GetCaps", "Couldn't get a property list in GetCaps.");

    // Loop through the retrieved format list.
    // For each format, get a list of format configurations.
    SAFEARRAY* formatList = pvFormatsSupported.parray;
    WMDM_FORMATCODE formatCode = WMDM_FORMATCODE_NOTUSED;
    for(LONG iCap = 0; iCap < formatList->rgsabound[0].cElements; iCap++)
    { 
        // Get a format from the SAFEARRAY of retrieved formats.
        SafeArrayGetElement(formatList, &iCap, &formatCode);

        // Call a custom function to see the specifics of device support for 
       // each format.
        if (formatCode != WMDM_FORMATCODE_NOTUSED)
            myGetFormatCaps(formatCode, pDevice);
    }

e_Exit:
    // Clear out the memory we used.
    PropVariantClear(&pvFormatsSupported);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/WMDM/enumerating-devices">Enumerating Devices</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3">IWMDMDevice3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty">IWMDMDevice3::SetProperty</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata">IWMDMStorage3::GetMetadata</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata">IWMDMStorage4::GetSpecifiedMetadata</a>



<a href="/windows/desktop/WMDM/setting-metadata-on-a-file">Setting Metadata on a File</a>