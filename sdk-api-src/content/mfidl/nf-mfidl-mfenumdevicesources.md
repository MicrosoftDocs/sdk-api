---
UID: NF:mfidl.MFEnumDeviceSources
title: MFEnumDeviceSources function (mfidl.h)
description: Enumerates a list of audio or video capture devices.
helpviewer_keywords: ["MFEnumDeviceSources","MFEnumDeviceSources function [Media Foundation]","MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE","MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE","MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY","mf.mfenumdevicesources","mfidl/MFEnumDeviceSources"]
old-location: mf\mfenumdevicesources.htm
tech.root: mf
ms.assetid: da4d96ce-e22b-4e1c-aa2e-df46416a5f0b
ms.date: 12/05/2018
ms.keywords: MFEnumDeviceSources, MFEnumDeviceSources function [Media Foundation], MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE, MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY, mf.mfenumdevicesources, mfidl/MFEnumDeviceSources
req.header: mfidl.h
req.include-header: 
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFEnumDeviceSources
 - mfidl/MFEnumDeviceSources
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFEnumDeviceSources
---

# MFEnumDeviceSources function


## -description

Enumerates a list of audio or video capture devices.

## -parameters

### -param pAttributes [in]

Pointer to an attribute store that contains search criteria. To create the attribute store, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a>. Set one or more of the following attributes on the attribute store:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE"></a><a id="mf_devsource_attribute_source_type"></a><dl>
<dt><b><a href="/windows/desktop/medfound/mf-devsource-attribute-source-type">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE</a></b></dt>
</dl>
</td>
<td width="60%">
Specifies whether to enumerate audio or video devices. (Required.)

</td>
</tr>
<tr>
<td width="40%"><a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE"></a><a id="mf_devsource_attribute_source_type_audcap_role"></a><dl>
<dt><b><a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-audcap-role">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE</a></b></dt>
</dl>
</td>
<td width="60%">
For audio capture devices, specifies the device role. (Optional.)

</td>
</tr>
<tr>
<td width="40%"><a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY"></a><a id="mf_devsource_attribute_source_type_vidcap_category"></a><dl>
<dt><b><a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-vidcap-category">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY</a></b></dt>
</dl>
</td>
<td width="60%">
For video capture devices, specifies the device category. (Optional.)

</td>
</tr>
</table>

### -param pppSourceActivate [out]

Receives an array of <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface pointers. Each pointer represents an activation object for a media source. The function allocates the memory for the array. The caller must release the pointers in the array and call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to free the memory for the array.

### -param pcSourceActivate [out]

Receives the number of elements in the <i>pppSourceActivate</i> array. If no capture devices match the search criteria, this parameter receives the value 0.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Each returned <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointer represents a capture device, and can be used to create a media source for that device. You can also use the <b>IMFActivate</b> pointer to query for attributes that describe the device. The following attributes might be set:

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-devsource-attribute-friendly-name">MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME</a>
</td>
<td>The display name of the device.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-devsource-attribute-media-type">MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE</a>
</td>
<td>The major type and subtype GUIDs that describe the device's output format.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-devsource-attribute-source-type">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE</a>
</td>
<td>The type of capture device (audio or video).</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-audcap-endpoint-id">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID</a>
</td>
<td>The audio endpoint ID string. (Audio devices only.)</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-vidcap-category">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY</a>
</td>
<td>The device category. (Video devices only.)</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-vidcap-hw-source">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE</a>
</td>
<td> Whether a device is a hardware or software device. (Video devices only.)</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-vidcap-symbolic-link">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK</a>
</td>
<td>The symbolic link for the device driver. (Video devices only.)</td>
</tr>
</table>
 

To create a media source from an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointer, call the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> method.


#### Examples

The following example enumerates the video capture devices on the system and creates a media source for the first device on the list.


```cpp
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/audio-video-capture-in-media-foundation">Audio/Video Capture in Media Foundation</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>