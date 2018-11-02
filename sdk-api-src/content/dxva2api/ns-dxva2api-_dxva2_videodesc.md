---
UID: NS:dxva2api._DXVA2_VideoDesc
title: "_DXVA2_VideoDesc"
author: windows-sdk-content
description: Describes a video stream for a DXVA decoder device or video processor device.
old-location: mf\dxva2_videodesc.htm
tech.root: medfound
ms.assetid: 0e500a08-a3b5-475c-8bbc-e4b30cce247d
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 0e500a08-a3b5-475c-8bbc-e4b30cce247d, DXVA2_VideoDesc, DXVA2_VideoDesc structure [Media Foundation], _DXVA2_VideoDesc, dxva2api/DXVA2_VideoDesc, mf.dxva2_videodesc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_VideoDesc
product: Windows
targetos: Windows
req.typenames: DXVA2_VideoDesc
req.redist: 
---

# _DXVA2_VideoDesc structure


## -description


Describes a video stream for a DXVA decoder device or video processor device.
        


## -struct-fields




### -field SampleWidth

Width of the video frame, in pixels.
          


### -field SampleHeight

Height of the video frame, in pixels.
          


### -field SampleFormat

Additional details about the video format, specified as a <a href="https://msdn.microsoft.com/eba2c56b-8951-4dc5-91ae-1371793ce787">DXVA2_ExtendedFormat</a> structure.
          


### -field Format

Surface format, specified as a <b>D3DFORMAT</b> value or FOURCC code. A FOURCC code can be constructed using the <b>D3DFORMAT</b> or <b>MAKEFOURCC</b> macros.
          


### -field InputSampleFreq

Frame rate of the input video stream, specified as a <a href="https://msdn.microsoft.com/03b6bef9-c0ba-4efa-9552-55c8e9fd77ae">DXVA2_Frequency</a> structure.
          


### -field OutputFrameFreq

Frame rate of the output video, specified as a <a href="https://msdn.microsoft.com/03b6bef9-c0ba-4efa-9552-55c8e9fd77ae">DXVA2_Frequency</a> structure.
          


### -field UABProtectionLevel

Level of data protection required when the user accessible bus (UAB) is present. If <b>TRUE</b>, the video must be protected when a UAB is present. If <b>FALSE</b>, the video is not required to be protected.
          


### -field Reserved

Reserved. Must be zero.
          


## -remarks



The <b>InputSampleFreq</b> member gives the frame rate of the decoded video stream, as received by the video renderer. The <b>OutputFrameFreq</b> member gives the frame rate of the video that is displayed after deinterlacing. If the input video is interlaced and the samples contain interleaved fields, the output frame rate is twice the input frame rate. If the input video is progressive or contains single fields, the output frame rate is the same as the input frame rate.

Decoders should set the values of <b>InputSampleFreq</b> and <b>OutputFrameFreq</b> if the frame rate is known. Otherwise, set these members to 0/0 to indicate an unknown frame rate.


#### Examples

The following code converts a Media Foundation media type, represented using the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface, into a <b>DXVA2_VideoDesc</b> structure.


```cpp
// Fills in the DXVA2_ExtendedFormat structure.
void GetDXVA2ExtendedFormatFromMFMediaType(
    IMFMediaType *pType, 
    DXVA2_ExtendedFormat *pFormat
)
{
    // Get the interlace mode.
    MFVideoInterlaceMode interlace = 
        (MFVideoInterlaceMode)MFGetAttributeUINT32(
            pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Unknown
         );

    // The values for interlace mode translate directly, except for mixed 
    // interlace or progressive mode.

    if (interlace == MFVideoInterlace_MixedInterlaceOrProgressive)
    {
        // Default to interleaved fields.
        pFormat->SampleFormat = DXVA2_SampleFieldInterleavedEvenFirst;
    }
    else
    {
        pFormat->SampleFormat = (UINT)interlace;
    }

    // The remaining values translate directly.
    
    // Use the "no-fail" attribute functions and default to "unknown."
    
    pFormat->VideoChromaSubsampling = MFGetAttributeUINT32(
        pType, MF_MT_VIDEO_CHROMA_SITING, MFVideoChromaSubsampling_Unknown);

    pFormat->NominalRange = MFGetAttributeUINT32(
        pType, MF_MT_VIDEO_NOMINAL_RANGE, MFNominalRange_Unknown);

    pFormat->VideoTransferMatrix = MFGetAttributeUINT32(
        pType, MF_MT_YUV_MATRIX, MFVideoTransferMatrix_Unknown);

    pFormat->VideoLighting = MFGetAttributeUINT32(
        pType, MF_MT_VIDEO_LIGHTING, MFVideoLighting_Unknown);

    pFormat->VideoPrimaries = MFGetAttributeUINT32(
        pType, MF_MT_VIDEO_PRIMARIES, MFVideoPrimaries_Unknown);

    pFormat->VideoTransferFunction = MFGetAttributeUINT32(
        pType, MF_MT_TRANSFER_FUNCTION, MFVideoTransFunc_Unknown);

}


HRESULT ConvertMFTypeToDXVAType(IMFMediaType *pType, DXVA2_VideoDesc *pDesc)
{
    ZeroMemory(pDesc, sizeof(*pDesc));

    GUID                    subtype = GUID_NULL;
    UINT32                  width = 0;
    UINT32                  height = 0;
    UINT32                  fpsNumerator = 0;
    UINT32                  fpsDenominator = 0;

    // The D3D format is the first DWORD of the subtype GUID.
    HRESULT hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    pDesc->Format = (D3DFORMAT)subtype.Data1;

    // Frame size.
    hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
    if (FAILED(hr))
    {
        goto done;
    }

    pDesc->SampleWidth = width;
    pDesc->SampleHeight = height;

    // Frame rate.
    hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, &fpsNumerator, &fpsDenominator);
    if (FAILED(hr))
    {
        goto done;
    }

    pDesc->InputSampleFreq.Numerator = fpsNumerator;
    pDesc->InputSampleFreq.Denominator = fpsDenominator;

    // Extended format information.
    GetDXVA2ExtendedFormatFromMFMediaType(pType, &pDesc->SampleFormat);

    // For progressive or single-field types, the output frequency is the same as
    // the input frequency. For interleaved-field types, the output frequency is
    // twice the input frequency.  
    pDesc->OutputFrameFreq = pDesc->InputSampleFreq;

    if ((pDesc->SampleFormat.SampleFormat == DXVA2_SampleFieldInterleavedEvenFirst) ||
        (pDesc->SampleFormat.SampleFormat == DXVA2_SampleFieldInterleavedOddFirst))
    {
        pDesc->OutputFrameFreq.Numerator *= 2;
    }

done:
    return hr;
}

```





## -see-also




<a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

