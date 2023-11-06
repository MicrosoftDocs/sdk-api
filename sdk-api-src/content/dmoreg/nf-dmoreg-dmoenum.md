---
UID: NF:dmoreg.DMOEnum
title: DMOEnum function (dmoreg.h)
description: The DMOEnum function enumerates DMOs listed in the registry. The caller can search by category, media type, or both.
helpviewer_keywords: ["DMOEnum","DMOEnum function [DirectShow]","dmoreg/DMOEnum","dshow.dmoenum"]
old-location: dshow\dmoenum.htm
tech.root: dshow
ms.assetid: 2cb69d28-15be-44fb-a180-98b560848c08
ms.date: 4/26/2023
ms.keywords: DMOEnum, DMOEnum function [DirectShow], dmoreg/DMOEnum, dshow.dmoenum
req.header: dmoreg.h
req.include-header: Dmo.h
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
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DMOEnum
 - dmoreg/DMOEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdmo.dll
api_name:
 - DMOEnum
---

# DMOEnum function


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DMOEnum</b> function enumerates DMOs listed in the registry. The caller can search by category, media type, or both.

## -parameters

### -param guidCategory

GUID that specifies which category of DMO to search. Use GUID_NULL to search every category. See <a href="/windows/desktop/DirectShow/dmo-guids">DMO GUIDs</a> for a list of category GUIDs.

### -param dwFlags

Bitwise combination of zero or more flags from the DMO_ENUM_FLAGS enumeration.

### -param cInTypes

Number of input media types to use in the search criteria. Use zero to match any input type.

### -param pInTypes

Pointer to an array of <a href="/previous-versions/windows/desktop/api/dmoreg/ns-dmoreg-dmo_partial_mediatype">DMO_PARTIAL_MEDIATYPE</a> structures that contain the input media types. Specify the size of the array in the cInTypes parameter.

### -param cOutTypes

Number of output media types to use in the search criteria. Use zero to match any output type.

### -param pOutTypes

Pointer to an array of DMO_PARTIAL_MEDIATYPE structures that contain the output media types. Specify the size of the array in the cOutTypes parameter.

### -param ppEnum

Address of a variable to receive the <a href="/windows/desktop/api/mediaobj/nn-mediaobj-ienumdmo">IEnumDMO</a> interface of the enumerator.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

This method returns a pointer to an enumerator object that supports the <a href="/windows/desktop/api/mediaobj/nn-mediaobj-ienumdmo">IEnumDMO</a> interface. The application uses the <b>IEnumDMO</b> interface to enumerate over the set of DMOs that match the search criteria.


#### Examples

The following example enumerates all audio effect DMOs on the user's system, including keyed DMOs.


```
IEnumDMO* pEnum = NULL; 
HRESULT hr = DMOEnum(
    DMOCATEGORY_AUDIO_EFFECT, // Category
    DMO_ENUMF_INCLUDE_KEYED,  // Included keyed DMOs
    0, NULL,                  // Input types (don't care)
    0, NULL,                  // Output types (don't care)
    &pEnum);

if (SUCCEEDED(hr)) 
{
    CLSID clsidDMO;
    WCHAR* wszName;
    do
    {
        hr = pEnum->Next(1, &clsidDMO, &wszName, NULL);
        if (hr == S_OK) 
        {  
            // Now wszName holds the friendly name of the DMO, 
            // and clsidDMO holds the CLSID. 

            // Remember to release wszName!
            CoTaskMemFree(wszName);
        }
    } while (hr == S_OK);
    pEnum->Release();
}

```

## -see-also

<a href="/windows/desktop/DirectShow/dmo-functions">DMO Functions</a>