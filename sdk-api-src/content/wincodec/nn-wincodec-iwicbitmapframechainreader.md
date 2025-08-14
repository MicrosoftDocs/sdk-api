---
UID: NN:wincodec.IWICBitmapFrameChainReader
title: IWICBitmapFrameChainReader
description: Provides access to frames that are linked to the current frame through chains of different types.
ms.date: 07/18/2025
tech.root: wic
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: wincodec.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wincodec.h
api_name:
 - IWICBitmapFrameChainReader
f1_keywords:
 - IWICBitmapFrameChainReader
 - wincodec/IWICBitmapFrameChainReader
dev_langs:
 - c++
helpviewer_keywords:
 - IWICBitmapFrameChainReader
---

## -description

Provides access to frames that are linked to the current frame through chains of different types.

To provide access to subordinate frames, the frame object (which is represented by [IWICBitmapFrameDecode](./nn-wincodec-iwicbitmapframedecode.md)), implements **IWICBitmapFrameChainReader**.

## -remarks

**IWICBitmapFrameChainReader** represents one of a set of COM interfaces that allow WIC to expose chains of linked frames, of different types.

The decoder for an image file can provide multiple frames. Each frame represents a separate image. Similarly, the encoder can accept multiple frames, and encode them into a single file. For example,  when scanning a multi-page document into TIFF format, the [IWICBitmapEncoder::CreateNewFrame](./nf-wincodec-iwicbitmapencoder-createnewframe.md) method is used to create a frame for each scanned page, and the [IWICBitmapDecoder::GetFrame](./nf-wincodec-iwicbitmapdecoder-getframe.md) method is used to retrieve each frame. In that scenario, there's no hierarchy of frames (each frame is just as important as another). Some image formats&mdash;such as HEIF and JPEG XL&mdash;support secondary frames that are linked to a primary frame. **IWICBitmapFrameChainReader** gives you a way to specify such relationships between frames in the WIC API. Examples of secondary frames include thumbnail images, preview images, and alpha plane bitmaps.

HEIF supports layered images (also known as *overlay images*). An overlay image is composed of multiple *layer* images that are stacked on top of each other in a specified order. The overlay image is the primary image, and the layer images are secondary (subordinate) images that are linked to the primary image. The layer images aren't typically displayed, but there are cases where an image-editing app needs to be able to read and write each individual layer image.

An overlay image requires metadata to describe how to compose the different layers into a single image. You can work with that metadata with WIC metadata interfaces such as [IWICMetadataReader](/windows/win32/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader) and [IWICMetadataWriter](/windows/win32/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter).

An overlay image often require lossless compression, because that allows image editing apps to open and save a file multiple times without degrading the image quality. The HEVC and AV1 compression formats for HEIF image files are lossy. With the WIC encoding APIs, you can use HEIF with uncompressed formats such as RGBA.

### Nesting

While **IWICBitmapFrameDecode** has a [GetThumbnail](./nf-wincodec-iwicbitmapframedecode-getthumbnail.md) method, and **IWICBitmapDecoder** has a [GetPreview](./nf-wincodec-iwicbitmapdecoder-getpreview.md) method&mdash;to return a thumbnail and a preview image, respectively&mdash;those methods return only a single image of each type. And those methods return the images as a bitmap rather than as a frame; which means that metadata and color space information is not available.

**IWICBitmapFrameChainReader** supports multiple frames of each type, and the frames can be nested. So, for example, a frame from an *Alternate* chain (see [WICBitmapChainType](./ne-wincodec-wicbitmapchaintype.md)) might itself have for example a *Preview* chain linked to it, or a **Layer** chain. Or a frame from a *Thumbnail* chain might have an *AlphaMap* chain or a *GainMap* chain.

WIC allows nesting of frames up to only 5 levels deep.

It's your responsibility as the caller to add frames in the correct order, and to create chains that serve a useful purpose. For example, adding frames to the *Preview* chain in the wrong order will still work, but it might not result in the optimal image-rendering experience in all cases. Similarly, it's possible to add multiple frames to the *GainMap* chain, but in practice only the first frame in that chain will be used. 

### Nesting

**IWICBitmapFrameChainReader** and [IWICBitmapFrameChainWriter](./nn-wincodec-iwicbitmapframechainwriter.md) are supported by HEIF and JPEG XL. HEIF supports all chain types, but JPEG XL supports only *Preview*, *Thumbnail* and *GainMap*. Attempts to encode a JPEG XL image with an unsupported chain type will result in a **WINCODEC_ERR_UNSUPPORTEDOPERATION** error. You can use the [IWICBitmapFrameChainWriter::DoesSupportChainType](./nf-wincodec-iwicbitmapframechainwriter-doessupportchaintype.md) method to determine whether a given chain type is supported by the encoder.

> [!NOTE]
> If a frame doesn't have a chain of a given type, then [IWICBitmapFrameChainReader::GetChainedFrameCount](./nf-wincodec-iwicbitmapframechainreader-getchainedframecount.md) will still succeed, but it will return a count of zero.

### Metadata for layered images

Layered images are specific to the HEIF format, defined in ISO/IEC 23008-12, where they're known as *Overlay images*. The [WICHeifProperties](./ne-wincodec-wicheifproperties.md) enumeration has the relevant constants **WICHeifLayeredImageCanvasColor** and **WICHeifLayeredImageLayerPositions**.

See Example 1 and Example 2.

### Lossless encoding for HEIF

For lossless encoding in the HEIF format, you can use the enum constant [WICHeifCompressionNone](./ne-wincodec-wicheifcompressionoption.md). For example, an encoding app can specify the **WICHeifCompressionNone** option, and invoke [IWICBitmapFrameEncode::WritePixels](./nf-wincodec-iwicbitmapframeencode-writepixels.md) or [WriteSource](./nf-wincodec-iwicbitmapframeencode-writesource.md) with a bitmap in the **GUID_WICPixelFormat32bppRGBA** format.

The [WICHeifCompressionOption](./ne-wincodec-wicheifcompressionoption.md) enumeration has the relevant constants **WICHeifCompressionJpegXL**, **WICHeifCompressionBrotli**, and **WICHeifCompressionDeflate**.

### Examples

#### Example 1: Decode a layered image

This example shows how to determine whether an image is a layered image (known as an *overlay image* in the HEIF file format). The example shows how to query for the metadata, and how to find each layer frame, which is needed to compose the layered image.

The example uses the [IWICMetadataReader](/windows/win32/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader) interface, which will work on all versions of Windows 11 where HEIF is supported.

```cpp
#include <wil/com.h>
#include <wincodec.h>

// This function finds the IWICMetadataReader for HEIF-specific metadata.
HRESULT GetHeifMetadataReader(
    _In_ IWICBitmapFrameDecode* frame,
    _COM_Outptr_ IWICMetadataReader** reader)
{
    *reader = nullptr;

    wil::com_ptr_nothrow<IWICMetadataBlockReader> blockReader;
    RETURN_IF_FAILED(wil::com_query_to_nothrow(frame, &blockReader));

    UINT numberOfReaders;
    RETURN_IF_FAILED(blockReader->GetCount(&numberOfReaders));

    for (UINT index = 0; index < numberOfReaders; index++)
    {
        wil::com_ptr_nothrow<IWICMetadataReader> metadataReader;
        RETURN_IF_FAILED(blockReader->GetReaderByIndex(index, &metadataReader));

        GUID metadataFormat;
        RETURN_IF_FAILED(metadataReader->GetMetadataFormat(&metadataFormat));
        if (metadataFormat == GUID_MetadataFormatHeif)
        {
            *reader = metadataReader.detach();
            return S_OK;
        }
    }

    return E_NOT_SET;
}

HRESULT DisplayFrame(_In_ IWICBitmapFrameDecode* primaryFrame)
{
    // To determine whether this is a layered image, we need to find the
    // HEIF-specific metadata.
    wil::com_ptr_nothrow<IWICMetadataReader> metadataReader;
    if (SUCCEEDED(GetHeifMetadataReader(primaryFrame, &metadataReader)))
    {
        PROPVARIANT propertyId{};
        propertyId.vt = VT_UI2;

        propertyId.uiVal = WICHeifLayeredImageCanvasColor;
        wil::unique_prop_variant propvariant;
        (void)metadataReader->GetValue(nullptr, &propertyId, &propvariant);

        if (propvariant.vt == VT_UI4)
        {
            // We got the color of the canvas.
            WICColor canvasColor = propvariant.ulVal;

            // Get the size of the canvas.
            UINT canvasWidth;
            UINT canvasHeight;
            RETURN_IF_FAILED(primaryFrame->GetSize(&canvasWidth, &canvasHeight));

            // Draw an empty canvas (not shown.)
            RETURN_IF_FAILED(RenderEmptyCanvas(canvasWidth, canvasHeight, canvasColor));

            // Get the position on the canvas of each layer image.
            propertyId.uiVal = WICHeifLayeredImageLayerPositions;
            propvariant.reset();
            (void)metadataReader->GetValue(nullptr, &propertyId, &propvariant);

            UINT layerPositionCount = 0;
            POINT* layerPositions = nullptr;

            if (propvariant.vt == (VT_VECTOR | VT_UI8))
            {
                layerPositionCount = propvariant.cauh.cElems;
                layerPositions = reinterpret_cast<POINT*>(propvariant.cauh.pElems);
            }

            // Check whether there are any layer frames chained to the primary frame.
            // If there are none, then we have just a blank canvas.
            wil::com_ptr_nothrow<IWICBitmapFrameChainReader> chainReader;
            if (SUCCEEDED(wil::com_query_to_nothrow(primaryFrame, &chainReader)))
            {
                UINT layerCount = 0;
                (void)chainReader->GetChainedFrameCount(WICBitmapChainType_Layer, &layerCount);

                // Render each layer.
                for (UINT layerIndex = 0; layerIndex < layerCount; ++layerIndex)
                {
                    wil::com_ptr_nothrow<IWICBitmapFrameDecode> layerFrame;
                    RETURN_IF_FAILED(chainReader->GetChainedFrame(WICBitmapChainType_Layer, layerIndex,
                        &layerFrame));

                    // If we don't have layer positions for some layers, then the default position
                    // is [0,0].
                    POINT layerPosition = (layerIndex < layerPositionCount) ? 
                        layerPositions[layerIndex] : POINT{ 0, 0 };

                    // The "DisplayLayerFrame" function is omitted for brevity.
                    RETURN_IF_FAILED(DisplayLayerFrame(layerFrame.get(), canvasWidth, canvasHeight, 
                        layerPosition.x, layerPosition.y));
                }
            }
        }
        else
        {
            // If we get here, then the WICHeifLayeredImageCanvasColor property is not present.
            // That property is required for layered frames. That means that the primary frame is not a
            // layered frame, and we should render it as a normal frame.
            // (Function not shown for brevity.)
            RETURN_IF_FAILED(DisplayNormalFrame(primaryFrame));
        }
    }
    else
    {
        // If we get here, then the IWICMetadataReader for HEIF is not available.
        // This means that the frame is not from a HEIF file, and it is definitely not a layered frame.
        RETURN_IF_FAILED(DisplayNormalFrame(primaryFrame));
    }
    return S_OK;
}
```

#### Example 2: Decode a layered image

This example shows how to decode a layered image using the [IWICMetadataQueryReader](./nn-wincodec-iwicmetadataqueryreader.md). The example is functionally equivalent to the previous example. Some parts that would be the same as in the previous example have been omitted to avoid repetition. The main difference is the use of **IWICMetadataQueryReader** instead of [IWICMetadataReader](./nn-wincodec-iwicmetadataqueryreader.md). While **IWICMetadataQueryReader** is easier to use, the disadvantage is that the **IWICMetadataQueryReader** supports querying for only layered image metadata on Windows 11 version 25H2, and later. So using **IWICMetadataQueryReader** on older versions of Windows than that will result in the [**GetMetadataByName**](./nf-wincodec-iwicmetadataqueryreader-getmetadatabyname.md) method returning an error.

```cpp
#include <wil/com.h>
#include <wincodec.h>

HRESULT DisplayFrame(_In_ IWICBitmapFrameDecode* primaryFrame)
{
    wil::com_ptr_nothrow<IWICMetadataQueryReader> metadataQueryReader;
    RETURN_IF_FAILED(primaryFrame->GetMetadataQueryReader(&metadataQueryReader));

    wil::unique_prop_variant propvariant;
    (void)metadataQueryReader->GetMetadataByName(L"/heifProps/LayeredImageCanvasColor", &propvariant);

    if (propvariant.vt == VT_UI4)
    {
        // We got the color of the canvas.
        WICColor canvasColor = propvariant.ulVal;

        // Get the position on the canvas of each layer image.
        propvariant.reset();
        (void)metadataQueryReader->GetMetadataByName(L"/heifProps/LayeredImageLayerPositions", &propvariant);

        UINT layerPositionCount = 0;
        POINT* layerPositions = nullptr;

        if (propvariant.vt == (VT_VECTOR | VT_UI8))
        {
            layerPositionCount = propvariant.cauh.cElems;
            layerPositions = reinterpret_cast<POINT*>(propvariant.cauh.pElems);
        }

        // Draw the canvas, and display each layer image (if any).
        // Function not shown for brevity.
        RETURN_IF_FAILED(DisplayCanvasAndAllLayers(primaryFrame, canvasColor, layerPositionCount, 
            layerPositions));
    }
    else
    {
        // If we get here, then we were unable to find the "/heifProps/LayeredImageCanvasColor" property,
        // probably because it's not present in the file.
        // That property is required for layered frames. That suggests that the primary frame is not a
        // layered frame. We will render it as a normal frame.
        // (Function not shown for brevity.)
        RETURN_IF_FAILED(DisplayNormalFrame(primaryFrame));
    }
    return S_OK;
}
```

#### Example 3: Encode a layered image

This example shows how to encode a layered image using the [IWICMetadataQueryWriter](./nn-wincodec-iwicmetadataquerywriter.md) and [IWICBitmapFrameChainWriter](./nn-wincodec-iwicbitmapframechainwriter.md).

```cpp
#include <wil/com.h>
#include <wincodec.h>

HRESULT CreateLayerImage(
    _In_ IWICImagingFactory* factory,
    _In_ IWICStream* outputStream,
    const SIZE& canvasSize,
    WICColor canvasColor,
    UINT numLayers,
    _In_reads_(numLayers) const POINT* layerPositions,
    _In_reads_(numLayers) IWICBitmapSource* layerBitmaps[])
{
    wil::com_ptr_nothrow<IWICBitmapEncoder> heifEncoder;
    RETURN_IF_FAILED(factory->CreateEncoder(GUID_ContainerFormatHeif, nullptr, &heifEncoder));

    RETURN_IF_FAILED(heifEncoder->Initialize(outputStream, WICBitmapEncoderCacheInMemory));

    wil::com_ptr_nothrow<IWICBitmapFrameEncode> layeredFrame;
    RETURN_IF_FAILED(heifEncoder->CreateNewFrame(&layeredFrame, nullptr));
    RETURN_IF_FAILED(layeredFrame->Initialize(nullptr));

    RETURN_IF_FAILED(layeredFrame->SetSize(canvasSize.cx, canvasSize.cy));

    // Create a chain of layer images, chained to the layered image.
    wil::com_ptr_nothrow<IWICBitmapFrameChainWriter> chainWriter;
    RETURN_IF_FAILED(wil::com_query_to_nothrow(layeredFrame, &chainWriter));

    for (ULONG layerIndex = 0; layerIndex < numLayers; ++layerIndex)
    {
        wil::com_ptr_nothrow<IWICBitmapFrameEncode> layerFrame;

        RETURN_IF_FAILED(chainWriter->AppendFrameToChain(WICBitmapChainType_Layer, layerFrame.get()));
        RETURN_IF_FAILED(layerFrame->Initialize(nullptr));

        RETURN_IF_FAILED(layerFrame->WriteSource(layerBitmaps[layerIndex], nullptr));
        RETURN_IF_FAILED(layerFrame->Commit());
    }

    // Write the background color and the position of each layer as metadata on the layered image.
    // (The chain and the metadata can also be added in opposite order to that shown here).
    wil::com_ptr_nothrow<IWICMetadataQueryWriter> queryWriter;
    RETURN_IF_FAILED(layeredFrame->GetMetadataQueryWriter(&queryWriter));

    PROPVARIANT propvariant{};
    propvariant.vt = VT_UI4;
    propvariant.ulVal = canvasColor;

    if (SUCCEEDED(queryWriter->SetMetadataByName(L"/heifProps/LayeredImageCanvasColor", &propvariant)))
    {
        propvariant.vt = VT_VECTOR | VT_UI8;
        propvariant.cauh.cElems = numLayers;
        propvariant.cauh.pElems = reinterpret_cast<ULARGE_INTEGER*>(layerPositions);  

        RETURN_IF_FAILED(queryWriter->SetMetadataByName(L"/heifProps/LayeredImageLayerPositions", 
            &propvariant));

        // Set the type to VT_EMPTY to avoid accidentally clearing the PROPVARIANT,
        // because cauh.pElems is pointing to memory not allocated with CoTaskMemAlloc.
        propvariant.vt = VT_EMPTY;
    }

    // Finalize the layered frame and the HEIF file.
    RETURN_IF_FAILED(layeredFrame->Commit());
    RETURN_IF_FAILED(heifEncoder->Commit());
    return S_OK;
}
```

#### Example 4: Encode an alternate frame

This example shows how your app can save an uncompressed frame by using lossless Deflate compression, while providing a lower quality alternative encoding using HEVC. Uncompressed images in HEIF is defined in a new standard that might not be supported outside Windows. This means that there's a possibility that a photo viewing app, especially one not running on Windows, won't be able to decode uncompressed frames. By providing an alternate frame encoded in HEVC, apps that don't support uncompressed frames will still be able to display the image, albeit at a lower quality.

```cpp
#include <wil/com.h>
#include <wincodec.h>

HRESULT AddUncompressedFrameWithHevcAlternate(
    _In_ IWICBitmapEncoder* heifEncoder,
    _In_ IWICBitmapSource* sourceBitmap)
{
    wil::com_ptr_nothrow<IWICBitmapFrameEncode> primaryFrame;
    wil::com_ptr_nothrow<IPropertyBag2> encoderOptions;
    RETURN_IF_FAILED(heifEncoder->CreateNewFrame(&primaryFrame, &encoderOptions));

    // Specify that the primary frame should be saved in uncompressed format with lossless Deflate compression applied to it.
    PROPBAG2 option{};
    option.pstrName = L"HeifCompressionMethod";

    wil::unique_variant prop;
    prop.vt = VT_UI1;
    prop.bVal = (BYTE)WICHeifCompressionDeflate;

    RETURN_IF_FAILED(primaryFrame->Initialize(encoderOptions.get()));
    RETURN_IF_FAILED(primaryFrame->WriteSource(sourceBitmap, nullptr));

    // Now create a chain of alternate frames, chained to the primary image.
    wil::com_ptr_nothrow<IWICBitmapFrameChainWriter> chainWriter;
    RETURN_IF_FAILED(wil::com_query_to_nothrow(primaryFrame, &chainWriter));

    // Create an alternate frame that is encoded using HEVC. This frame will be displayed by
    // photo viewing apps when uncompressed images aren't supported.
    // HEVC is the default, so we don't need to specify any encoding options for this frame.
    wil::com_ptr_nothrow<IWICBitmapFrameEncode> alternateFrame;
    RETURN_IF_FAILED(chainWriter->AppendFrameToChain(WICBitmapChainType_Alternate, &alternateFrame,
        nullptr));
    RETURN_IF_FAILED(alternateFrame->Initialize(nullptr));
    RETURN_IF_FAILED(alternateFrame->WriteSource(sourceBitmap, nullptr));
    RETURN_IF_FAILED(alternateFrame->Commit());

    RETURN_IF_FAILED(primaryFrame->Commit());
    RETURN_IF_FAILED(heifEncoder->Commit());
    return S_OK;
}
```

#### Example 5: Checking whether gain map chains are supported

This example shows how your app can check whether the encoder supports storing a gain map with the primary image. If the primary image is in standard-dynamic-range (SDR) format, then a gain map can be used to enhance the primary image to high-dynamic-range (HDR). But not all file formats support gain maps, so your app might first want to check whether gain maps are supported before spending resources on generating the gain map. This example shows how you can do that by using the [IWICBitmapFrameChainWriter::DoesSupportChainType](./nf-wincodec-iwicbitmapframechainwriter-doessupportchaintype.md) method.

```cpp
#include <wil/com.h>
#include <wincodec.h>

HRESULT EncodeHdrBitmap(
    _In_ IWICBitmapEncoder* encoder,
    _In_ IWICBitmapSource* hdrBitmap)
{
    wil::com_ptr_nothrow<IWICBitmapFrameEncode> primaryFrame;
    wil::com_ptr_nothrow<IWICBitmapFrameEncode> gainMapFrame;
    wil::com_ptr_nothrow<IWICBitmapFrameChainWriter> chainWriter;

    RETURN_IF_FAILED(encoder->CreateNewFrame(&primaryFrame, nullptr));

    if (SUCCEEDED(wil::com_query_to_nothrow(primaryFrame, &chainWriter)))
    {
        // Check whether this encoder supports adding a gain map.
        BOOL isSupported;
        if (SUCCEEDED(chainWriter->DoesSupportChainType(WICBitmapChainType_GainMap, &isSupported)) &&
            isSupported)
        {
            RETURN_IF_FAILED(chainWriter->AppendFrameToChain(WICBitmapChainType_GainMap, &gainMapFrame,
                nullptr));
            RETURN_IF_FAILED(gainMapFrame->Initialize(nullptr));

            // Split the HDR frame into a base image (written to primaryFrame) and a gain map.
            // (This function is not shown, for brevity).
            RETURN_IF_FAILED(SplitHdrBitmapIntoSdrAndGainMap(hdrBitmap, primaryFrame.get(), 
                gainMapFrame.get()));
        }
    }

    if (gainMapFrame != nullptr)
    {
        // We successfully created a separate frame for the gain map. Commit the changes to the file.
        RETURN_IF_FAILED(gainMapFrame->Commit());
    }
    else
    {
        // The encoder doesn't support gain maps, so we write the full HDR image as a single frame. 
        RETURN_IF_FAILED(primaryFrame->WriteSource(hdrBitmap, nullptr));
    }

    RETURN_IF_FAILED(primaryFrame->Commit());
    RETURN_IF_FAILED(encoder->Commit());
    return S_OK;
}
```

## -see-also

* [IWICBitmapFrameChainWriter](./nn-wincodec-iwicbitmapframechainwriter.md)
