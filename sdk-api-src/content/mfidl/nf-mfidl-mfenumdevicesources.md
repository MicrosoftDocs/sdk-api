---
UID: NF:mfidl.MFEnumDeviceSources
title: MFEnumDeviceSources function
author: windows-sdk-content
description: Enumerates a list of audio or video capture devices.
old-location: mf\mfenumdevicesources.htm
tech.root: medfound
ms.assetid: da4d96ce-e22b-4e1c-aa2e-df46416a5f0b
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFEnumDeviceSources, MFEnumDeviceSources function [Media Foundation], MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE, MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY, mf.mfenumdevicesources, mfidl/MFEnumDeviceSources
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFEnumDeviceSources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFEnumDeviceSources function


## -description


Enumerates a list of audio or video capture devices.


## -parameters




### -param pAttributes [in]

Pointer to an attribute store that contains search criteria. To create the attribute store, call <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a>. Set one or more of the following attributes on the attribute store:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE"></a><a id="mf_devsource_attribute_source_type"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/c6c05267-1c93-48e2-b463-b5a1514f1b7b">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE</a></b></dt>
</dl>
</td>
<td width="60%">
Specifies whether to enumerate audio or video devices. (Required.)

</td>
</tr>
<tr>
<td width="40%"><a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE"></a><a id="mf_devsource_attribute_source_type_audcap_role"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/4f2885b6-c771-4577-880d-5feea671432e">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE</a></b></dt>
</dl>
</td>
<td width="60%">
For audio capture devices, specifies the device role. (Optional.)

</td>
</tr>
<tr>
<td width="40%"><a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY"></a><a id="mf_devsource_attribute_source_type_vidcap_category"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/008ff9df-ebe0-4efd-a62c-24f4a4239ebd">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY</a></b></dt>
</dl>
</td>
<td width="60%">
For video capture devices, specifies the device category. (Optional.)

</td>
</tr>
</table>
 


### -param pppSourceActivate [out]

Receives an array of <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface pointers. Each pointer represents an activation object for a media source. The function allocates the memory for the array. The caller must release the pointers in the array and call <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to free the memory for the array.


### -param pcSourceActivate [out]

Receives the number of elements in the <i>pppSourceActivate</i> array. If no capture devices match the search criteria, this parameter receives the value 0.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each returned <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> pointer represents a capture device, and can be used to create a media source for that device. You can also use the <b>IMFActivate</b> pointer to query for attributes that describe the device. The following attributes might be set:

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3f6c7faf-2ecd-4510-adc2-252c3619d70f">MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME</a>
</td>
<td>The display name of the device.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/33a1b546-ece2-44ef-a1c0-5579c32be0bc">MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE</a>
</td>
<td>The major type and subtype GUIDs that describe the device's output format.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c6c05267-1c93-48e2-b463-b5a1514f1b7b">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE</a>
</td>
<td>The type of capture device (audio or video).</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a0d8b54b-7a05-4307-a756-a34bb22f1afd">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID</a>
</td>
<td>The audio endpoint ID string. (Audio devices only.)</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/008ff9df-ebe0-4efd-a62c-24f4a4239ebd">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY</a>
</td>
<td>The device category. (Video devices only.)</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4a886124-54f1-4cd1-a22b-552e8c8d556f">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE</a>
</td>
<td> Whether a device is a hardware or software device. (Video devices only.)</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3d256dec-ec8c-4c62-883b-e2c292fd90eb">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK</a>
</td>
<td>The symbolic link for the device driver. (Video devices only.)</td>
</tr>
</table>
 

To create a media source from an <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> pointer, call the <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> method.


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




<a href="https://msdn.microsoft.com/8a9d96f8-1096-4b66-a2ec-8a95d754ea72">Audio/Video Capture in Media Foundation</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

