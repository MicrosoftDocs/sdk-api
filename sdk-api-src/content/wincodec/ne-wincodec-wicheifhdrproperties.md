---
UID: NE:wincodec.WICHeifHdrProperties
title: WICHeifHdrProperties
description: Specifies the HDR properties of a High Efficiency Image Format (HEIF) image.
helpviewer_keywords: ["WICHeifHdrProperties"]
tech.root: wic
ms.date: 01/31/2019
ms.keywords: WICHeifHdrProperties
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: wincodec.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 1903 [desktop apps only]
req.target-min-winversvr: Windows Server, version 1903 [desktop apps only]
req.target-type: Windows
req.typenames: 
req.umdf-ver: 
ms.custom: 19H1
f1_keywords:
 - WICHeifHdrProperties
 - wincodec/WICHeifHdrProperties
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wincodec.h
api_name:
 - WICHeifHdrProperties
---

## -description

Specifies the HDR properties of a High Efficiency Image Format (HEIF) image.

## -enum-fields

### -field WICHeifHdrMaximumLuminanceLevel:0x1

[VT_UI2] Specifies the maximum luminance level of the content in Nits.

### -field WICHeifHdrMaximumFrameAverageLuminanceLevel:0x2

[VT_UI2] Specifies the maximum average per-frame luminance level of the content in Nits.

### -field WICHeifHdrMinimumMasteringDisplayLuminanceLevel:0x3

[VT_UI2] Specifies the maximum luminance of the display on which the content was authored, in Nits.

### -field WICHeifHdrMaximumMasteringDisplayLuminanceLevel:0x4

[VT_UI2] Specifies the maximum luminance of the display on which the content was authored, in Nits.

### -field WICHeifHdrCustomVideoPrimaries:0x5

[VT_BLOB] Specifies custom color primaries for a video media type. The value of this property is a [MT_CUSTOM_VIDEO_PRIMARIES](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries)structure, returned as an array of bytes (VT_BLOB).

### -field WICHeifHdrProperties_FORCE_DWORD:0x7fffffff

## -remarks

Use [IWicMetadataReader::GetValue](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatareader-getvalue) to retrieve the value of the properties specified with this enumeration. Instantiate the **IWicMetadataReader** instance using the GUID **CLSID_WICMetadataReader**. Call [IWicMetadataReader::GetMetadataFormat](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatareader-getmetadataformat) and confirm that the value is **GUID_MetadataFormatHeifHDR** to verify that the metadata format is HEIF HDR metadata. 

Not all HEIF HDR images will have all of these properties present in the file, so only those properties that are available will be exposed by the metadata reader. 

```cpp
using namespace winrt;

std::optional<uint32_t> GetMaximumLuminanceLevelFromMetadataReader(_In_ IWICMetadataReader* metadataReader)
{
    std::optional<uint32_t> result;
    GUID metadataFormat;

    // Retrieve the format of the metadata used by this IWICMetadataReader
    check_hresult(metadataReader->GetMetadataFormat(&metadataFormat));

    // This function only handles HEIF HDR metadata
    if (metadataFormat != GUID_MetadataFormatHeifHDR)
    {
        throw_hresult(E_INVALIDARG);
    }

    PROPVARIANT variantId = {};
    PROPVARIANT variantValue = {};

    variantId.vt = VT_UI4;
    variantId.uiVal = WICHeifHdrMaximumLuminanceLevel;
    if (SUCCEEDED(metadataReader->GetValue(nullptr, &variantId, &variantValue)))
    {
        if (variantValue.vt == VT_UI4)
        {
            result = variantValue.uiVal;
        }
        PropVariantClear(&variantValue);
    }

    return result;
}
```

## -see-also
