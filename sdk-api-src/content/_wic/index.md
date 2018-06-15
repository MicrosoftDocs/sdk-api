---
UID: TP:wic
ms.assetid: 4b34c381-d2c6-3b09-91ab-1f2c0f240d8b
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Windows Imaging Component

## -description

Overview of the Windows Imaging Component technology.

To develop Windows Imaging Component, you need these headers:

 * [wincodec.h](../wincodec/index.md)
 * [wincodecsdk.h](../wincodecsdk/index.md)

For the programming guide, see [Windows Imaging Component](/windows/desktop/wic).

## Functions

| Title   | Description   |
| ---- |:---- |
| [WICConvertBitmapSource function](..\wincodec\nf-wincodec-wicconvertbitmapsource.md) | Obtains a IWICBitmapSource in the desired pixel format from a given IWICBitmapSource. |
| [WICCreateBitmapFromSection function](..\wincodec\nf-wincodec-wiccreatebitmapfromsection.md) | Returns a IWICBitmapSource that is backed by the pixels of a Windows Graphics Device Interface (GDI) section handle. |
| [WICCreateBitmapFromSectionEx function](..\wincodec\nf-wincodec-wiccreatebitmapfromsectionex.md) | Returns a IWICBitmapSource that is backed by the pixels of a Windows Graphics Device Interface (GDI) section handle. |
| [WICGetMetadataContentSize function](..\wincodecsdk\nf-wincodecsdk-wicgetmetadatacontentsize.md) | Returns the size of the metadata content contained by the specified IWICMetadataWriter. The returned size accounts for the header and the length of the metadata. |
| [WICMapGuidToShortName function](..\wincodec\nf-wincodec-wicmapguidtoshortname.md) | Obtains the short name associated with a given GUID. |
| [WICMapSchemaToName function](..\wincodec\nf-wincodec-wicmapschematoname.md) | Obtains the name associated with a given schema. |
| [WICMapShortNameToGuid function](..\wincodec\nf-wincodec-wicmapshortnametoguid.md) | Obtains the GUID associated with the given short name. |
| [WICMatchMetadataContent function](..\wincodecsdk\nf-wincodecsdk-wicmatchmetadatacontent.md) | Obtains a metadata format GUID for a specified container format and vendor that best matches the content within a given stream. |
| [WICSerializeMetadataContent function](..\wincodecsdk\nf-wincodecsdk-wicserializemetadatacontent.md) | Writes metadata into a given stream. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [PFNProgressNotification callback function](..\wincodec\nc-wincodec-pfnprogressnotification.md) | Application defined callback function called when codec component progress is made. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [WICBitmapPattern structure](..\wincodec\ns-wincodec-wicbitmappattern.md) | Contains members that identify a pattern within an image file which can be used to identify a particular format. |
| [WICBitmapPlane structure](..\wincodec\ns-wincodec-wicbitmapplane.md) | Specifies the pixel format, buffer, stride and size of a component plane for a planar pixel format. |
| [WICBitmapPlaneDescription structure](..\wincodec\ns-wincodec-wicbitmapplanedescription.md) | Specifies the pixel format and size of a component plane. |
| [WICDdsFormatInfo structure](..\wincodec\ns-wincodec-wicddsformatinfo.md) | Specifies the DXGI_FORMAT and block information of a DDS format. |
| [WICDdsParameters structure](..\wincodec\ns-wincodec-wicddsparameters.md) | Specifies the DDS image dimension, DXGI_FORMAT and alpha mode of contained data. |
| [WICImageParameters structure](..\wincodec\ns-wincodec-wicimageparameters.md) | This defines parameters that you can use to override the default parameters normally used when encoding an image. |
| [WICJpegFrameHeader structure](..\wincodec\ns-wincodec-wicjpegframeheader.md) | Represents a JPEG frame header. |
| [WICJpegScanHeader structure](..\wincodec\ns-wincodec-wicjpegscanheader.md) | Represents a JPEG frame header. |
| [WICMetadataHeader structure](..\wincodecsdk\ns-wincodecsdk-wicmetadataheader.md) | Represents metadata header. |
| [WICMetadataPattern structure](..\wincodecsdk\ns-wincodecsdk-wicmetadatapattern.md) | Represents a metadata pattern. |
| [WICRawCapabilitiesInfo structure](..\wincodec\ns-wincodec-wicrawcapabilitiesinfo.md) | Defines raw codec capabilites. |
| [WICRawToneCurve structure](..\wincodec\ns-wincodec-wicrawtonecurve.md) | Represents a raw image tone curve. |
| [WICRawToneCurvePoint structure](..\wincodec\ns-wincodec-wicrawtonecurvepoint.md) | Represents a raw image tone curve point. |
| [WICRect structure](..\wincodec\ns-wincodec-wicrect.md) | Represents a rectangle for Windows Imaging Component (WIC) API. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [WIC8BIMIptcDigestProperties enumeration](..\wincodec\ne-wincodec-wic8bimiptcdigestproperties.md) | Specifies the identifiers of the metadata items in an 8BIM IPTC digest metadata block. |
| [WIC8BIMIptcProperties enumeration](..\wincodec\ne-wincodec-wic8bimiptcproperties.md) | Specifies the identifiers of the metadata items in an 8BIM IPTC block. |
| [WIC8BIMResolutionInfoProperties enumeration](..\wincodec\ne-wincodec-wic8bimresolutioninfoproperties.md) | Specifies the identifiers of the metadata items in an 8BIMResolutionInfo block. |
| [WICBitmapAlphaChannelOption enumeration](..\wincodec\ne-wincodec-wicbitmapalphachanneloption.md) | Specifies the desired alpha channel usage. |
| [WICBitmapCreateCacheOption enumeration](..\wincodec\ne-wincodec-wicbitmapcreatecacheoption.md) | Specifies the desired cache usage. |
| [WICBitmapDecoderCapabilities enumeration](..\wincodec\ne-wincodec-wicbitmapdecodercapabilities.md) | Specifies the capabilities of the decoder. |
| [WICBitmapDitherType enumeration](..\wincodec\ne-wincodec-wicbitmapdithertype.md) | Specifies the type of dither algorithm to apply when converting between image formats. |
| [WICBitmapEncoderCacheOption enumeration](..\wincodec\ne-wincodec-wicbitmapencodercacheoption.md) | Specifies the cache options available for an encoder. |
| [WICBitmapInterpolationMode enumeration](..\wincodec\ne-wincodec-wicbitmapinterpolationmode.md) | Specifies the sampling or filtering mode to use when scaling an image. |
| [WICBitmapLockFlags enumeration](..\wincodec\ne-wincodec-wicbitmaplockflags.md) | Specifies access to an IWICBitmap. |
| [WICBitmapPaletteType enumeration](..\wincodec\ne-wincodec-wicbitmappalettetype.md) | Specifies the type of palette used for an indexed image format. |
| [WICBitmapTransformOptions enumeration](..\wincodec\ne-wincodec-wicbitmaptransformoptions.md) | Specifies the flip and rotation transforms. |
| [WICColorContextType enumeration](..\wincodec\ne-wincodec-wiccolorcontexttype.md) | Specifies the color context types. |
| [WICComponentEnumerateOptions enumeration](..\wincodec\ne-wincodec-wiccomponentenumerateoptions.md) | Specifies component enumeration options. |
| [WICComponentSigning enumeration](..\wincodec\ne-wincodec-wiccomponentsigning.md) | Specifies the component signing status. |
| [WICComponentType enumeration](..\wincodec\ne-wincodec-wiccomponenttype.md) | Specifies the type of Windows Imaging Component (WIC) component. |
| [WICDdsAlphaMode enumeration](..\wincodec\ne-wincodec-wicddsalphamode.md) | Specifies the the meaning of pixel color component values contained in the DDS image. |
| [WICDdsDimension enumeration](..\wincodec\ne-wincodec-wicddsdimension.md) | Specifies the dimension type of the data contained in DDS image. |
| [WICDecodeOptions enumeration](..\wincodec\ne-wincodec-wicdecodeoptions.md) | Specifies decode options. |
| [WICGifApplicationExtensionProperties enumeration](..\wincodec\ne-wincodec-wicgifapplicationextensionproperties.md) | Specifies the application extension metadata properties for a Graphics Interchange Format (GIF) image. |
| [WICGifCommentExtensionProperties enumeration](..\wincodec\ne-wincodec-wicgifcommentextensionproperties.md) | Specifies the comment extension metadata properties for a Graphics Interchange Format (GIF) image. |
| [WICGifGraphicControlExtensionProperties enumeration](..\wincodec\ne-wincodec-wicgifgraphiccontrolextensionproperties.md) | Specifies the graphic control extension metadata properties that define the transitions between each frame animation for Graphics Interchange Format (GIF) images. |
| [WICGifImageDescriptorProperties enumeration](..\wincodec\ne-wincodec-wicgifimagedescriptorproperties.md) | Specifies the image descriptor metadata properties for Graphics Interchange Format (GIF) frames. |
| [WICGifLogicalScreenDescriptorProperties enumeration](..\wincodec\ne-wincodec-wicgiflogicalscreendescriptorproperties.md) | Specifies the logical screen descriptor properties for Graphics Interchange Format (GIF) metadata. |
| [WICJpegChrominanceProperties enumeration](..\wincodec\ne-wincodec-wicjpegchrominanceproperties.md) | Specifies the JPEG chrominance table property. |
| [WICJpegCommentProperties enumeration](..\wincodec\ne-wincodec-wicjpegcommentproperties.md) | Specifies the JPEG comment properties. |
| [WICJpegIndexingOptions enumeration](..\wincodec\ne-wincodec-wicjpegindexingoptions.md) | Specifies the options for indexing a JPEG image. |
| [WICJpegLuminanceProperties enumeration](..\wincodec\ne-wincodec-wicjpegluminanceproperties.md) | Specifies the JPEG luminance table property. |
| [WICJpegScanType enumeration](..\wincodec\ne-wincodec-wicjpegscantype.md) | Specifies the memory layout of pixel data in a JPEG image scan. |
| [WICJpegTransferMatrix enumeration](..\wincodec\ne-wincodec-wicjpegtransfermatrix.md) | Specifies conversion matrix from Y'Cb'Cr' to R'G'B'. |
| [WICJpegYCrCbSubsamplingOption enumeration](..\wincodec\ne-wincodec-wicjpegycrcbsubsamplingoption.md) | Specifies the JPEG YCrCB subsampling options. |
| [WICMetadataCreationOptions enumeration](..\wincodecsdk\ne-wincodecsdk-wicmetadatacreationoptions.md) | Specifies metadata creation options. |
| [WICNamedWhitePoint enumeration](..\wincodec\ne-wincodec-wicnamedwhitepoint.md) | Specifies named white balances for raw images. |
| [WICPersistOptions enumeration](..\wincodecsdk\ne-wincodecsdk-wicpersistoptions.md) | Specifies Windows Imaging Component (WIC) options that are used when initializing a component with a stream. |
| [WICPixelFormatNumericRepresentation enumeration](..\wincodec\ne-wincodec-wicpixelformatnumericrepresentation.md) | WICPixelFormatNumericRepresentation enumeration |
| [WICPlanarOptions enumeration](..\wincodec\ne-wincodec-wicplanaroptions.md) | Specifies additional options to an IWICPlanarBitmapSourceTransform implementation. |
| [WICPngBkgdProperties enumeration](..\wincodec\ne-wincodec-wicpngbkgdproperties.md) | Specifies the Portable Network Graphics (PNG) background (bKGD) chunk metadata properties. |
| [WICPngChrmProperties enumeration](..\wincodec\ne-wincodec-wicpngchrmproperties.md) | Specifies the Portable Network Graphics (PNG) cHRM chunk metadata properties for CIE XYZ chromaticity. |
| [WICPngFilterOption enumeration](..\wincodec\ne-wincodec-wicpngfilteroption.md) | Specifies the Portable Network Graphics (PNG) filters available for compression optimization. |
| [WICPngGamaProperties enumeration](..\wincodec\ne-wincodec-wicpnggamaproperties.md) | Specifies the Portable Network Graphics (PNG) gAMA chunk metadata properties. |
| [WICPngHistProperties enumeration](..\wincodec\ne-wincodec-wicpnghistproperties.md) | Specifies the Portable Network Graphics (PNG) hIST chunk metadata properties. |
| [WICPngIccpProperties enumeration](..\wincodec\ne-wincodec-wicpngiccpproperties.md) | Specifies the Portable Network Graphics (PNG) iCCP chunk metadata properties. |
| [WICPngItxtProperties enumeration](..\wincodec\ne-wincodec-wicpngitxtproperties.md) | Specifies the Portable Network Graphics (PNG) iTXT chunk metadata properties. |
| [WICPngSrgbProperties enumeration](..\wincodec\ne-wincodec-wicpngsrgbproperties.md) | Specifies the Portable Network Graphics (PNG) sRGB chunk metadata properties. |
| [WICPngTimeProperties enumeration](..\wincodec\ne-wincodec-wicpngtimeproperties.md) | Specifies the Portable Network Graphics (PNG) tIME chunk metadata properties. |
| [WICProgressNotification enumeration](..\wincodec\ne-wincodec-wicprogressnotification.md) | Specifies when the progress notification callback should be called. |
| [WICProgressOperation enumeration](..\wincodec\ne-wincodec-wicprogressoperation.md) | Specifies the progress operations to receive notifications for. |
| [WICRawCapabilities enumeration](..\wincodec\ne-wincodec-wicrawcapabilities.md) | Specifies the capability support of a raw image. |
| [WICRawParameterSet enumeration](..\wincodec\ne-wincodec-wicrawparameterset.md) | Specifies the parameter set used by a raw codec. |
| [WICRawRenderMode enumeration](..\wincodec\ne-wincodec-wicrawrendermode.md) | Specifies the render intent of the next CopyPixels call. |
| [WICRawRotationCapabilities enumeration](..\wincodec\ne-wincodec-wicrawrotationcapabilities.md) | Specifies the rotation capabilities of the codec. |
| [WICSectionAccessLevel enumeration](..\wincodec\ne-wincodec-wicsectionaccesslevel.md) | Specifies the access level of a Windows Graphics Device Interface (GDI) section. |
| [WICTiffCompressionOption enumeration](..\wincodec\ne-wincodec-wictiffcompressionoption.md) | Specifies the Tagged Image File Format (TIFF) compression options. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IWICBitmap interface](..\wincodec\nn-wincodec-iwicbitmap.md) | Defines methods that add the concept of writeability and static in-memory representations of bitmaps to IWICBitmapSource. |
| [IWICBitmapClipper interface](..\wincodec\nn-wincodec-iwicbitmapclipper.md) | Exposes methods that produce a clipped version of the input bitmap for a specified rectangular region of interest. |
| [IWICBitmapCodecInfo interface](..\wincodec\nn-wincodec-iwicbitmapcodecinfo.md) | Exposes methods that provide information about a particular codec. |
| [IWICBitmapCodecProgressNotification interface](..\wincodec\nn-wincodec-iwicbitmapcodecprogressnotification.md) | Exposes methods used for progress notification for encoders and decoders. |
| [IWICBitmapDecoder interface](..\wincodec\nn-wincodec-iwicbitmapdecoder.md) | Exposes methods that represent a decoder. |
| [IWICBitmapDecoderInfo interface](..\wincodec\nn-wincodec-iwicbitmapdecoderinfo.md) | Exposes methods that provide information about a decoder. |
| [IWICBitmapEncoder interface](..\wincodec\nn-wincodec-iwicbitmapencoder.md) | Defines methods for setting an encoder's properties such as thumbnails, frames, and palettes. |
| [IWICBitmapEncoderInfo interface](..\wincodec\nn-wincodec-iwicbitmapencoderinfo.md) | Exposes methods that provide information about an encoder. |
| [IWICBitmapFlipRotator interface](..\wincodec\nn-wincodec-iwicbitmapfliprotator.md) | Exposes methods that produce a flipped (horizontal or vertical) and/or rotated (by 90 degree increments) bitmap source. Rotations are done before the flip. |
| [IWICBitmapFrameDecode interface](..\wincodec\nn-wincodec-iwicbitmapframedecode.md) | Defines methods for decoding individual image frames of an encoded file. |
| [IWICBitmapFrameEncode interface](..\wincodec\nn-wincodec-iwicbitmapframeencode.md) | Represents an encoder's individual image frames. |
| [IWICBitmapLock interface](..\wincodec\nn-wincodec-iwicbitmaplock.md) | Exposes methods that support the Lock method. |
| [IWICBitmapScaler interface](..\wincodec\nn-wincodec-iwicbitmapscaler.md) | Represents a resized version of the input bitmap using a resampling or filtering algorithm. |
| [IWICBitmapSource interface](..\wincodec\nn-wincodec-iwicbitmapsource.md) | Exposes methods that refers to a source from which pixels are retrieved, but cannot be written back to. |
| [IWICBitmapSourceTransform interface](..\wincodec\nn-wincodec-iwicbitmapsourcetransform.md) | Exposes methods for offloading certain operations to the underlying IWICBitmapSource implementation. |
| [IWICColorContext interface](..\wincodec\nn-wincodec-iwiccolorcontext.md) | Exposes methods for color management. |
| [IWICColorTransform interface](..\wincodec\nn-wincodec-iwiccolortransform.md) | Exposes methods that transforms an IWICBitmapSource from one color context to another. |
| [IWICComponentFactory interface](..\wincodecsdk\nn-wincodecsdk-iwiccomponentfactory.md) | Exposes methods that create components used by component developers. This includes metadata readers, writers and other services for use by codec and metadata handler developers. |
| [IWICComponentInfo interface](..\wincodec\nn-wincodec-iwiccomponentinfo.md) | Exposes methods that provide component information. |
| [IWICDdsDecoder interface](..\wincodec\nn-wincodec-iwicddsdecoder.md) | Provides information and functionality specific to the DDS image format. |
| [IWICDdsEncoder interface](..\wincodec\nn-wincodec-iwicddsencoder.md) | Enables writing DDS format specific information to an encoder. |
| [IWICDdsFrameDecode interface](..\wincodec\nn-wincodec-iwicddsframedecode.md) | Provides access to a single frame of DDS image data in its native DXGI_FORMAT form, as well as information about the image data. |
| [IWICDevelopRaw interface](..\wincodec\nn-wincodec-iwicdevelopraw.md) | Exposes methods that provide access to the capabilites of a raw codec format. |
| [IWICDevelopRawNotificationCallback interface](..\wincodec\nn-wincodec-iwicdeveloprawnotificationcallback.md) | Exposes a callback method for raw image change nofications. |
| [IWICEnumMetadataItem interface](..\wincodec\nn-wincodec-iwicenummetadataitem.md) | Exposes methods that provide enumeration services for individual metadata items. |
| [IWICFastMetadataEncoder interface](..\wincodec\nn-wincodec-iwicfastmetadataencoder.md) | Exposes methods used for in-place metadata editing. A fast metadata encoder enables you to add and remove metadata to an image without having to fully re-encode the image. |
| [IWICFormatConverter interface](..\wincodec\nn-wincodec-iwicformatconverter.md) | Represents an IWICBitmapSource that converts the image data from one pixel format to another, handling dithering and halftoning to indexed formats, palette translation and alpha thresholding. |
| [IWICFormatConverterInfo interface](..\wincodec\nn-wincodec-iwicformatconverterinfo.md) | Exposes methods that provide information about a pixel format converter. |
| [IWICImageEncoder interface](..\wincodec\nn-wincodec-iwicimageencoder.md) | Encodes ID2D1Image interfaces to an IWICBitmapEncoder. |
| [IWICImagingFactory interface](..\wincodec\nn-wincodec-iwicimagingfactory.md) | Exposes methods used to create components for the Windows Imaging Component (WIC) such as decoders, encoders and pixel format converters. |
| [IWICImagingFactory2 interface](..\wincodec\nn-wincodec-iwicimagingfactory2.md) | An extension of the WIC factory interface that includes the ability to create an IWICImageEncoder. |
| [IWICJpegFrameDecode interface](..\wincodec\nn-wincodec-iwicjpegframedecode.md) | Exposes methods for decoding JPEG images. Provides access to the Start Of Frame (SOF) header, Start of Scan (SOS) header, the Huffman and Quantization tables, and the compressed JPEG JPEG data. Also enables indexing for efficient random access. |
| [IWICJpegFrameEncode interface](..\wincodec\nn-wincodec-iwicjpegframeencode.md) | Exposes methods for writing compressed JPEG scan data directly to the WIC encoder's output stream. Also provides access to the Huffman and quantization tables. |
| [IWICMetadataBlockReader interface](..\wincodecsdk\nn-wincodecsdk-iwicmetadatablockreader.md) | Exposes methods that provide access to all of the codec's top level metadata blocks. |
| [IWICMetadataBlockWriter interface](..\wincodecsdk\nn-wincodecsdk-iwicmetadatablockwriter.md) | Exposes methods that enable the encoding of metadata. This interface is implemented by the decoder and its image frames. |
| [IWICMetadataHandlerInfo interface](..\wincodecsdk\nn-wincodecsdk-iwicmetadatahandlerinfo.md) | Exposes methods that provide basic information about the registered metadata handler. |
| [IWICMetadataQueryReader interface](..\wincodec\nn-wincodec-iwicmetadataqueryreader.md) | Exposes methods for retrieving metadata blocks and items from a decoder or its image frames using a metadata query expression. |
| [IWICMetadataQueryWriter interface](..\wincodec\nn-wincodec-iwicmetadataquerywriter.md) | Exposes methods for setting or removing metadata blocks and items to an encoder or its image frames using a metadata query expression. |
| [IWICMetadataReader interface](..\wincodecsdk\nn-wincodecsdk-iwicmetadatareader.md) | Exposes methods that provide access to underlining metadata content. This interface is implemented by independent software vendors (ISVs) to create new metadata readers. |
| [IWICMetadataReaderInfo interface](..\wincodecsdk\nn-wincodecsdk-iwicmetadatareaderinfo.md) | Exposes methods that provide basic information about the registered metadata reader. |
| [IWICMetadataWriter interface](..\wincodecsdk\nn-wincodecsdk-iwicmetadatawriter.md) | Exposes methods that provide access to writing metadata content. This is implemented by independent software vendors (ISVs) to create new metadata writers. |
| [IWICMetadataWriterInfo interface](..\wincodecsdk\nn-wincodecsdk-iwicmetadatawriterinfo.md) | Exposes methods that provide basic information about the registered metadata writer. |
| [IWICPalette interface](..\wincodec\nn-wincodec-iwicpalette.md) | Exposes methods for accessing and building a color table, primarily for indexed pixel formats. |
| [IWICPersistStream interface](..\wincodecsdk\nn-wincodecsdk-iwicpersiststream.md) | Exposes methods that provide additional load and save methods that take WICPersistOptions. |
| [IWICPixelFormatInfo interface](..\wincodec\nn-wincodec-iwicpixelformatinfo.md) | Exposes methods that provide information about a pixel format. |
| [IWICPixelFormatInfo2 interface](..\wincodec\nn-wincodec-iwicpixelformatinfo2.md) | Extends IWICPixelFormatInfo by providing additional information about a pixel format. |
| [IWICPlanarBitmapFrameEncode interface](..\wincodec\nn-wincodec-iwicplanarbitmapframeencode.md) | Allows planar component image pixels to be written to an encoder. |
| [IWICPlanarBitmapSourceTransform interface](..\wincodec\nn-wincodec-iwicplanarbitmapsourcetransform.md) | Provides access to planar Y’CbCr pixel formats where pixel components are stored in separate component planes. |
| [IWICPlanarFormatConverter interface](..\wincodec\nn-wincodec-iwicplanarformatconverter.md) | Allows a format converter to be initialized with a planar source. |
| [IWICProgressCallback interface](..\wincodec\nn-wincodec-iwicprogresscallback.md) | IWICProgressCallback interface is documented only for compliance; its use is not recommended and may be altered or unavailable in the future. Instead, and use RegisterProgressNotification. |
| [IWICProgressiveLevelControl interface](..\wincodec\nn-wincodec-iwicprogressivelevelcontrol.md) | Exposes methods for obtaining information about and controlling progressive decoding. |
| [IWICStream interface](..\wincodec\nn-wincodec-iwicstream.md) | Represents a Windows Imaging Component (WIC) stream for referencing imaging and metadata content. |
| [IWICStreamProvider interface](..\wincodecsdk\nn-wincodecsdk-iwicstreamprovider.md) | Exposes methods for a stream provider. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IWICBitmap::Lock](..\wincodec\nf-wincodec-iwicbitmap-lock.md) | Provides access to a rectangular area of the bitmap. |
| [IWICBitmap::SetPalette](..\wincodec\nf-wincodec-iwicbitmap-setpalette.md) | Provides access for palette modifications. |
| [IWICBitmap::SetResolution](..\wincodec\nf-wincodec-iwicbitmap-setresolution.md) | Changes the physical resolution of the image. |
| [IWICBitmapClipper::Initialize](..\wincodec\nf-wincodec-iwicbitmapclipper-initialize.md) | Initializes the bitmap clipper with the provided parameters. |
| [IWICBitmapCodecInfo::DoesSupportAnimation](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-doessupportanimation.md) | Retrieves a value indicating whether the codec supports animation. |
| [IWICBitmapCodecInfo::DoesSupportChromakey](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-doessupportchromakey.md) | Retrieves a value indicating whether the codec supports chromakeys. |
| [IWICBitmapCodecInfo::DoesSupportLossless](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-doessupportlossless.md) | Retrieves a value indicating whether the codec supports lossless formats. |
| [IWICBitmapCodecInfo::DoesSupportMultiframe](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe.md) | Retrieves a value indicating whether the codec supports multi frame images. |
| [IWICBitmapCodecInfo::GetColorManagementVersion](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-getcolormanagementversion.md) | Retrieves the color manangement version number the codec supports. |
| [IWICBitmapCodecInfo::GetContainerFormat](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-getcontainerformat.md) | Retrieves the container GUID associated with the codec. |
| [IWICBitmapCodecInfo::GetDeviceManufacturer](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer.md) | Retrieves the name of the device manufacture associated with the codec. |
| [IWICBitmapCodecInfo::GetDeviceModels](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-getdevicemodels.md) | Retrieves a comma delimited list of device models associated with the codec. |
| [IWICBitmapCodecInfo::GetFileExtensions](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-getfileextensions.md) | Retrieves a comma delimited list of the file name extensions associated with the codec. |
| [IWICBitmapCodecInfo::GetMimeTypes](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-getmimetypes.md) | Retrieves a comma delimited sequence of mime types associated with the codec. |
| [IWICBitmapCodecInfo::GetPixelFormats](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-getpixelformats.md) | Retrieves the pixel formats the codec supports. |
| [IWICBitmapCodecInfo::MatchesMimeType](..\wincodec\nf-wincodec-iwicbitmapcodecinfo-matchesmimetype.md) | Retrieves a value indicating whether the given mime type matches the mime type of the codec. |
| [IWICBitmapCodecProgressNotification::RegisterProgressNotification](..\wincodec\nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification.md) | Registers a progress notification callback function. |
| [IWICBitmapDecoder::CopyPalette](..\wincodec\nf-wincodec-iwicbitmapdecoder-copypalette.md) | Copies the decoder's IWICPalette . |
| [IWICBitmapDecoder::GetColorContexts](..\wincodec\nf-wincodec-iwicbitmapdecoder-getcolorcontexts.md) | Retrieves the IWICColorContext objects of the image. |
| [IWICBitmapDecoder::GetContainerFormat](..\wincodec\nf-wincodec-iwicbitmapdecoder-getcontainerformat.md) | Retrieves the image's container format. |
| [IWICBitmapDecoder::GetDecoderInfo](..\wincodec\nf-wincodec-iwicbitmapdecoder-getdecoderinfo.md) | Retrieves an IWICBitmapDecoderInfo for the image. |
| [IWICBitmapDecoder::GetFrameCount](..\wincodec\nf-wincodec-iwicbitmapdecoder-getframecount.md) | Retrieves the total number of frames in the image. |
| [IWICBitmapDecoder::GetFrame](..\wincodec\nf-wincodec-iwicbitmapdecoder-getframe.md) | Retrieves the specified frame of the image. |
| [IWICBitmapDecoder::GetMetadataQueryReader](..\wincodec\nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader.md) | Retrieves the metadata query reader from the decoder. |
| [IWICBitmapDecoder::GetPreview](..\wincodec\nf-wincodec-iwicbitmapdecoder-getpreview.md) | Retrieves a preview image, if supported. |
| [IWICBitmapDecoder::GetThumbnail](..\wincodec\nf-wincodec-iwicbitmapdecoder-getthumbnail.md) | Retrieves a bitmap thumbnail of the image, if one exists |
| [IWICBitmapDecoder::Initialize](..\wincodec\nf-wincodec-iwicbitmapdecoder-initialize.md) | Initializes the decoder with the provided stream. |
| [IWICBitmapDecoder::QueryCapability](..\wincodec\nf-wincodec-iwicbitmapdecoder-querycapability.md) | Retrieves the capabilities of the decoder based on the specified stream. |
| [IWICBitmapDecoderInfo::CreateInstance](..\wincodec\nf-wincodec-iwicbitmapdecoderinfo-createinstance.md) | Creates a new IWICBitmapDecoder instance. |
| [IWICBitmapDecoderInfo::GetPatterns](..\wincodec\nf-wincodec-iwicbitmapdecoderinfo-getpatterns.md) | Retrieves the file pattern signatures supported by the decoder. |
| [IWICBitmapDecoderInfo::MatchesPattern](..\wincodec\nf-wincodec-iwicbitmapdecoderinfo-matchespattern.md) | Retrieves a value that indicates whether the codec recognizes the pattern within a specified stream. |
| [IWICBitmapEncoder::Commit](..\wincodec\nf-wincodec-iwicbitmapencoder-commit.md) | Commits all changes for the image and closes the stream. |
| [IWICBitmapEncoder::CreateNewFrame](..\wincodec\nf-wincodec-iwicbitmapencoder-createnewframe.md) | Creates a new IWICBitmapFrameEncode instance. |
| [IWICBitmapEncoder::GetContainerFormat](..\wincodec\nf-wincodec-iwicbitmapencoder-getcontainerformat.md) | Retrieves the encoder's container format. |
| [IWICBitmapEncoder::GetEncoderInfo](..\wincodec\nf-wincodec-iwicbitmapencoder-getencoderinfo.md) | Retrieves an IWICBitmapEncoderInfo for the encoder. |
| [IWICBitmapEncoder::GetMetadataQueryWriter](..\wincodec\nf-wincodec-iwicbitmapencoder-getmetadataquerywriter.md) | Retrieves a metadata query writer for the encoder. |
| [IWICBitmapEncoder::Initialize](..\wincodec\nf-wincodec-iwicbitmapencoder-initialize.md) | Initializes the encoder with an IStream which tells the encoder where to encode the bits. |
| [IWICBitmapEncoder::SetColorContexts](..\wincodec\nf-wincodec-iwicbitmapencoder-setcolorcontexts.md) | Sets the IWICColorContext objects for the encoder. |
| [IWICBitmapEncoder::SetPalette](..\wincodec\nf-wincodec-iwicbitmapencoder-setpalette.md) | Sets the global palette for the image. |
| [IWICBitmapEncoder::SetPreview](..\wincodec\nf-wincodec-iwicbitmapencoder-setpreview.md) | Sets the global preview for the image. |
| [IWICBitmapEncoder::SetThumbnail](..\wincodec\nf-wincodec-iwicbitmapencoder-setthumbnail.md) | Sets the global thumbnail for the image. |
| [IWICBitmapEncoderInfo::CreateInstance](..\wincodec\nf-wincodec-iwicbitmapencoderinfo-createinstance.md) | Creates a new IWICBitmapEncoder instance. |
| [IWICBitmapFlipRotator::Initialize](..\wincodec\nf-wincodec-iwicbitmapfliprotator-initialize.md) | Initializes the bitmap flip rotator with the provided parameters. |
| [IWICBitmapFrameDecode::GetColorContexts](..\wincodec\nf-wincodec-iwicbitmapframedecode-getcolorcontexts.md) | Retrieves the IWICColorContext associated with the image frame. |
| [IWICBitmapFrameDecode::GetMetadataQueryReader](..\wincodec\nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader.md) | Retrieves a metadata query reader for the frame. |
| [IWICBitmapFrameDecode::GetThumbnail](..\wincodec\nf-wincodec-iwicbitmapframedecode-getthumbnail.md) | Retrieves a small preview of the frame, if supported by the codec. |
| [IWICBitmapFrameEncode::Commit](..\wincodec\nf-wincodec-iwicbitmapframeencode-commit.md) | Commits the frame to the image. |
| [IWICBitmapFrameEncode::GetMetadataQueryWriter](..\wincodec\nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter.md) | Gets the metadata query writer for the encoder frame. |
| [IWICBitmapFrameEncode::Initialize](..\wincodec\nf-wincodec-iwicbitmapframeencode-initialize.md) | Initializes the frame encoder using the given properties. |
| [IWICBitmapFrameEncode::SetColorContexts](..\wincodec\nf-wincodec-iwicbitmapframeencode-setcolorcontexts.md) | Sets a given number IWICColorContext profiles to the frame. |
| [IWICBitmapFrameEncode::SetPalette](..\wincodec\nf-wincodec-iwicbitmapframeencode-setpalette.md) | Sets the IWICPalette for indexed pixel formats. |
| [IWICBitmapFrameEncode::SetPixelFormat](..\wincodec\nf-wincodec-iwicbitmapframeencode-setpixelformat.md) | Requests that the encoder use the specified pixel format. |
| [IWICBitmapFrameEncode::SetResolution](..\wincodec\nf-wincodec-iwicbitmapframeencode-setresolution.md) | Sets the physical resolution of the output image. |
| [IWICBitmapFrameEncode::SetSize](..\wincodec\nf-wincodec-iwicbitmapframeencode-setsize.md) | Sets the output image dimensions for the frame. |
| [IWICBitmapFrameEncode::SetThumbnail](..\wincodec\nf-wincodec-iwicbitmapframeencode-setthumbnail.md) | Sets the frame thumbnail if supported by the codec. |
| [IWICBitmapFrameEncode::WritePixels](..\wincodec\nf-wincodec-iwicbitmapframeencode-writepixels.md) | Copies scan-line data from a caller-supplied buffer to the IWICBitmapFrameEncode object. |
| [IWICBitmapFrameEncode::WriteSource](..\wincodec\nf-wincodec-iwicbitmapframeencode-writesource.md) | Encodes a bitmap source. |
| [IWICBitmapLock::GetDataPointer](..\wincodec\nf-wincodec-iwicbitmaplock-getdatapointer.md) | Gets the pointer to the top left pixel in the locked rectangle. |
| [IWICBitmapLock::GetPixelFormat](..\wincodec\nf-wincodec-iwicbitmaplock-getpixelformat.md) | Gets the pixel format of for the locked area of pixels. This can be used to compute the number of bytes-per-pixel in the locked area. |
| [IWICBitmapLock::GetSize](..\wincodec\nf-wincodec-iwicbitmaplock-getsize.md) | Retrieves the width and height, in pixels, of the locked rectangle. |
| [IWICBitmapLock::GetStride](..\wincodec\nf-wincodec-iwicbitmaplock-getstride.md) | Provides access to the stride value for the memory. |
| [IWICBitmapScaler::Initialize](..\wincodec\nf-wincodec-iwicbitmapscaler-initialize.md) | Initializes the bitmap scaler with the provided parameters. |
| [IWICBitmapSource::CopyPalette](..\wincodec\nf-wincodec-iwicbitmapsource-copypalette.md) | Retrieves the color table for indexed pixel formats. |
| [IWICBitmapSource::CopyPixels](..\wincodec\nf-wincodec-iwicbitmapsource-copypixels.md) | Instructs the object to produce pixels. |
| [IWICBitmapSource::GetPixelFormat](..\wincodec\nf-wincodec-iwicbitmapsource-getpixelformat.md) | Retrieves the pixel format of the bitmap source.. |
| [IWICBitmapSource::GetResolution](..\wincodec\nf-wincodec-iwicbitmapsource-getresolution.md) | Retrieves the sampling rate between pixels and physical world measurements. |
| [IWICBitmapSource::GetSize](..\wincodec\nf-wincodec-iwicbitmapsource-getsize.md) | Retrieves the pixel width and height of the bitmap. |
| [IWICBitmapSourceTransform::CopyPixels](..\wincodec\nf-wincodec-iwicbitmapsourcetransform-copypixels.md) | Copies pixel data using the supplied input parameters. |
| [IWICBitmapSourceTransform::DoesSupportTransform](..\wincodec\nf-wincodec-iwicbitmapsourcetransform-doessupporttransform.md) | Determines whether a specific transform option is supported natively by the implementation of the IWICBitmapSourceTransform interface. |
| [IWICBitmapSourceTransform::GetClosestPixelFormat](..\wincodec\nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat.md) | Retrieves the closest pixel format to which the implementation of IWICBitmapSourceTransform can natively copy pixels, given a desired format. |
| [IWICBitmapSourceTransform::GetClosestSize](..\wincodec\nf-wincodec-iwicbitmapsourcetransform-getclosestsize.md) | Returns the closest dimensions the implementation can natively scale to given the desired dimensions. |
| [IWICColorContext::GetExifColorSpace](..\wincodec\nf-wincodec-iwiccolorcontext-getexifcolorspace.md) | Retrieves the Exchangeable Image File (EXIF) color space color context. |
| [IWICColorContext::GetProfileBytes](..\wincodec\nf-wincodec-iwiccolorcontext-getprofilebytes.md) | Retrieves the color context profile. |
| [IWICColorContext::GetType](..\wincodec\nf-wincodec-iwiccolorcontext-gettype.md) | Retrieves the color context type. |
| [IWICColorContext::InitializeFromExifColorSpace](..\wincodec\nf-wincodec-iwiccolorcontext-initializefromexifcolorspace.md) | Initializes the color context using an Exchangeable Image File (EXIF) color space. |
| [IWICColorContext::InitializeFromFilename](..\wincodec\nf-wincodec-iwiccolorcontext-initializefromfilename.md) | Initializes the color context from the given file. |
| [IWICColorContext::InitializeFromMemory](..\wincodec\nf-wincodec-iwiccolorcontext-initializefrommemory.md) | Initializes the color context from a memory block. |
| [IWICColorTransform::Initialize](..\wincodec\nf-wincodec-iwiccolortransform-initialize.md) | Initializes an IWICColorTransform with a IWICBitmapSource and transforms it from one IWICColorContext to another. |
| [IWICComponentFactory::CreateEncoderPropertyBag](..\wincodecsdk\nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag.md) | Creates an encoder property bag. |
| [IWICComponentFactory::CreateMetadataReaderFromContainer](..\wincodecsdk\nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer.md) | Creates an IWICMetadataReader based on the given parameters. |
| [IWICComponentFactory::CreateMetadataReader](..\wincodecsdk\nf-wincodecsdk-iwiccomponentfactory-createmetadatareader.md) | Creates an IWICMetadataReader based on the given parameters. |
| [IWICComponentFactory::CreateMetadataWriterFromReader](..\wincodecsdk\nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader.md) | Creates an IWICMetadataWriter from the given IWICMetadataReader. |
| [IWICComponentFactory::CreateMetadataWriter](..\wincodecsdk\nf-wincodecsdk-iwiccomponentfactory-createmetadatawriter.md) | Creates an IWICMetadataWriter based on the given parameters. |
| [IWICComponentFactory::CreateQueryReaderFromBlockReader](..\wincodecsdk\nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader.md) | Creates a IWICMetadataQueryReader from the given IWICMetadataBlockReader. |
| [IWICComponentFactory::CreateQueryWriterFromBlockWriter](..\wincodecsdk\nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter.md) | Creates a IWICMetadataQueryWriter from the given IWICMetadataBlockWriter. |
| [IWICComponentInfo::GetAuthor](..\wincodec\nf-wincodec-iwiccomponentinfo-getauthor.md) | Retrieves the name of component's author. |
| [IWICComponentInfo::GetCLSID](..\wincodec\nf-wincodec-iwiccomponentinfo-getclsid.md) | Retrieves the component's class identifier (CLSID) |
| [IWICComponentInfo::GetComponentType](..\wincodec\nf-wincodec-iwiccomponentinfo-getcomponenttype.md) | Retrieves the component's WICComponentType. |
| [IWICComponentInfo::GetFriendlyName](..\wincodec\nf-wincodec-iwiccomponentinfo-getfriendlyname.md) | Retrieves the component's friendly name, which is a human-readable display name for the component. |
| [IWICComponentInfo::GetSigningStatus](..\wincodec\nf-wincodec-iwiccomponentinfo-getsigningstatus.md) | Retrieves the signing status of the component. |
| [IWICComponentInfo::GetSpecVersion](..\wincodec\nf-wincodec-iwiccomponentinfo-getspecversion.md) | Retrieves the component's specification version. |
| [IWICComponentInfo::GetVendorGUID](..\wincodec\nf-wincodec-iwiccomponentinfo-getvendorguid.md) | Retrieves the vendor GUID. |
| [IWICComponentInfo::GetVersion](..\wincodec\nf-wincodec-iwiccomponentinfo-getversion.md) | Retrieves the component's version. |
| [IWICDdsDecoder::GetFrame](..\wincodec\nf-wincodec-iwicddsdecoder-getframe.md) | Retrieves the specified frame of the DDS image. |
| [IWICDdsDecoder::GetParameters](..\wincodec\nf-wincodec-iwicddsdecoder-getparameters.md) | Gets DDS-specific data. |
| [IWICDdsEncoder::CreateNewFrame](..\wincodec\nf-wincodec-iwicddsencoder-createnewframe.md) | Creates a new frame to encode. |
| [IWICDdsEncoder::GetParameters](..\wincodec\nf-wincodec-iwicddsencoder-getparameters.md) | Gets DDS-specific data. |
| [IWICDdsEncoder::SetParameters](..\wincodec\nf-wincodec-iwicddsencoder-setparameters.md) | Sets DDS-specific data. |
| [IWICDdsFrameDecode::CopyBlocks](..\wincodec\nf-wincodec-iwicddsframedecode-copyblocks.md) | Requests pixel data as it is natively stored within the DDS file. |
| [IWICDdsFrameDecode::GetFormatInfo](..\wincodec\nf-wincodec-iwicddsframedecode-getformatinfo.md) | Gets information about the format in which the DDS image is stored. |
| [IWICDdsFrameDecode::GetSizeInBlocks](..\wincodec\nf-wincodec-iwicddsframedecode-getsizeinblocks.md) | Gets the width and height, in blocks, of the DDS image. |
| [IWICDevelopRaw::GetContrast](..\wincodec\nf-wincodec-iwicdevelopraw-getcontrast.md) | Gets the contrast value of the raw image. |
| [IWICDevelopRaw::GetCurrentParameterSet](..\wincodec\nf-wincodec-iwicdevelopraw-getcurrentparameterset.md) | Gets the current set of parameters. |
| [IWICDevelopRaw::GetExposureCompensation](..\wincodec\nf-wincodec-iwicdevelopraw-getexposurecompensation.md) | Gets the exposure compensation stop value of the raw image. |
| [IWICDevelopRaw::GetGamma](..\wincodec\nf-wincodec-iwicdevelopraw-getgamma.md) | Gets the current gamma setting of the raw image. |
| [IWICDevelopRaw::GetKelvinRangeInfo](..\wincodec\nf-wincodec-iwicdevelopraw-getkelvinrangeinfo.md) | Gets the information about the current Kelvin range of the raw image. |
| [IWICDevelopRaw::GetNamedWhitePoint](..\wincodec\nf-wincodec-iwicdevelopraw-getnamedwhitepoint.md) | Gets the named white point of the raw image. |
| [IWICDevelopRaw::GetNoiseReduction](..\wincodec\nf-wincodec-iwicdevelopraw-getnoisereduction.md) | Gets the noise reduction value of the raw image. |
| [IWICDevelopRaw::GetRenderMode](..\wincodec\nf-wincodec-iwicdevelopraw-getrendermode.md) | Gets the current WICRawRenderMode. |
| [IWICDevelopRaw::GetRotation](..\wincodec\nf-wincodec-iwicdevelopraw-getrotation.md) | Gets the current rotation angle. |
| [IWICDevelopRaw::GetSaturation](..\wincodec\nf-wincodec-iwicdevelopraw-getsaturation.md) | Gets the saturation value of the raw image. |
| [IWICDevelopRaw::GetSharpness](..\wincodec\nf-wincodec-iwicdevelopraw-getsharpness.md) | Gets the sharpness value of the raw image. |
| [IWICDevelopRaw::GetTint](..\wincodec\nf-wincodec-iwicdevelopraw-gettint.md) | Gets the tint value of the raw image. |
| [IWICDevelopRaw::GetToneCurve](..\wincodec\nf-wincodec-iwicdevelopraw-gettonecurve.md) | Gets the tone curve of the raw image. |
| [IWICDevelopRaw::GetWhitePointKelvin](..\wincodec\nf-wincodec-iwicdevelopraw-getwhitepointkelvin.md) | Gets the white point Kelvin temperature of the raw image. |
| [IWICDevelopRaw::GetWhitePointRGB](..\wincodec\nf-wincodec-iwicdevelopraw-getwhitepointrgb.md) | Gets the white point RGB values. |
| [IWICDevelopRaw::LoadParameterSet](..\wincodec\nf-wincodec-iwicdevelopraw-loadparameterset.md) | Sets the desired WICRawParameterSet option. |
| [IWICDevelopRaw::QueryRawCapabilitiesInfo](..\wincodec\nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo.md) | Retrieves information about which capabilities are supported for a raw image. |
| [IWICDevelopRaw::SetContrast](..\wincodec\nf-wincodec-iwicdevelopraw-setcontrast.md) | Sets the contrast value of the raw image. |
| [IWICDevelopRaw::SetDestinationColorContext](..\wincodec\nf-wincodec-iwicdevelopraw-setdestinationcolorcontext.md) | Sets the destination color context. |
| [IWICDevelopRaw::SetExposureCompensation](..\wincodec\nf-wincodec-iwicdevelopraw-setexposurecompensation.md) | Sets the exposure compensation stop value. |
| [IWICDevelopRaw::SetGamma](..\wincodec\nf-wincodec-iwicdevelopraw-setgamma.md) | Sets the desired gamma value. |
| [IWICDevelopRaw::SetNamedWhitePoint](..\wincodec\nf-wincodec-iwicdevelopraw-setnamedwhitepoint.md) | Sets the named white point of the raw file. |
| [IWICDevelopRaw::SetNoiseReduction](..\wincodec\nf-wincodec-iwicdevelopraw-setnoisereduction.md) | Sets the noise reduction value of the raw image. |
| [IWICDevelopRaw::SetNotificationCallback](..\wincodec\nf-wincodec-iwicdevelopraw-setnotificationcallback.md) | Sets the notification callback method. |
| [IWICDevelopRaw::SetRenderMode](..\wincodec\nf-wincodec-iwicdevelopraw-setrendermode.md) | Sets the current WICRawRenderMode. |
| [IWICDevelopRaw::SetRotation](..\wincodec\nf-wincodec-iwicdevelopraw-setrotation.md) | Sets the desired rotation angle. |
| [IWICDevelopRaw::SetSaturation](..\wincodec\nf-wincodec-iwicdevelopraw-setsaturation.md) | Sets the saturation value of the raw image. |
| [IWICDevelopRaw::SetSharpness](..\wincodec\nf-wincodec-iwicdevelopraw-setsharpness.md) | Sets the sharpness value of the raw image. |
| [IWICDevelopRaw::SetTint](..\wincodec\nf-wincodec-iwicdevelopraw-settint.md) | Sets the tint value of the raw image. |
| [IWICDevelopRaw::SetToneCurve](..\wincodec\nf-wincodec-iwicdevelopraw-settonecurve.md) | Sets the tone curve for the raw image. |
| [IWICDevelopRaw::SetWhitePointKelvin](..\wincodec\nf-wincodec-iwicdevelopraw-setwhitepointkelvin.md) | Sets the white point Kelvin value. |
| [IWICDevelopRaw::SetWhitePointRGB](..\wincodec\nf-wincodec-iwicdevelopraw-setwhitepointrgb.md) | Sets the white point RGB values. |
| [IWICDevelopRawNotificationCallback::Notify](..\wincodec\nf-wincodec-iwicdeveloprawnotificationcallback-notify.md) | An application-defined callback method used for raw image parameter change notifications. |
| [IWICEnumMetadataItem::Clone](..\wincodec\nf-wincodec-iwicenummetadataitem-clone.md) | Creates a copy of the current IWICEnumMetadataItem. |
| [IWICEnumMetadataItem::Next](..\wincodec\nf-wincodec-iwicenummetadataitem-next.md) | Advanced the current position in the enumeration. |
| [IWICEnumMetadataItem::Reset](..\wincodec\nf-wincodec-iwicenummetadataitem-reset.md) | Resets the current position to the beginning of the enumeration. |
| [IWICEnumMetadataItem::Skip](..\wincodec\nf-wincodec-iwicenummetadataitem-skip.md) | Skips to given number of objects. |
| [IWICFastMetadataEncoder::Commit](..\wincodec\nf-wincodec-iwicfastmetadataencoder-commit.md) | Finalizes metadata changes to the image stream. |
| [IWICFastMetadataEncoder::GetMetadataQueryWriter](..\wincodec\nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter.md) | Retrieves a metadata query writer for fast metadata encoding. |
| [IWICFormatConverter::CanConvert](..\wincodec\nf-wincodec-iwicformatconverter-canconvert.md) | Determines if the source pixel format can be converted to the destination pixel format. |
| [IWICFormatConverter::Initialize](..\wincodec\nf-wincodec-iwicformatconverter-initialize.md) | Initializes the format converter. |
| [IWICFormatConverterInfo::CreateInstance](..\wincodec\nf-wincodec-iwicformatconverterinfo-createinstance.md) | Creates a new IWICFormatConverter instance. |
| [IWICFormatConverterInfo::GetPixelFormats](..\wincodec\nf-wincodec-iwicformatconverterinfo-getpixelformats.md) | Retrieves a list of GUIDs that signify which pixel formats the converter supports. |
| [IWICImageEncoder::WriteFrameThumbnail](..\wincodec\nf-wincodec-iwicimageencoder-writeframethumbnail.md) | Encodes the image as a thumbnail to the frame given by the IWICBitmapFrameEncode. |
| [IWICImageEncoder::WriteFrame](..\wincodec\nf-wincodec-iwicimageencoder-writeframe.md) | Encodes the image to the frame given by the IWICBitmapFrameEncode. |
| [IWICImageEncoder::WriteThumbnail](..\wincodec\nf-wincodec-iwicimageencoder-writethumbnail.md) | Encodes the given image as the thumbnail to the given WIC bitmap encoder. |
| [IWICImagingFactory2::CreateImageEncoder](..\wincodec\nf-wincodec-iwicimagingfactory2-createimageencoder.md) | Creates a new image encoder object. |
| [IWICImagingFactory::CreateBitmapClipper](..\wincodec\nf-wincodec-iwicimagingfactory-createbitmapclipper.md) | Creates a new instance of an IWICBitmapClipper object. |
| [IWICImagingFactory::CreateBitmapFlipRotator](..\wincodec\nf-wincodec-iwicimagingfactory-createbitmapfliprotator.md) | Creates a new instance of an IWICBitmapFlipRotator object. |
| [IWICImagingFactory::CreateBitmapFromHBITMAP](..\wincodec\nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap.md) | Creates an IWICBitmap from a bitmap handle. |
| [IWICImagingFactory::CreateBitmapFromHICON](..\wincodec\nf-wincodec-iwicimagingfactory-createbitmapfromhicon.md) | Creates an IWICBitmap from an icon handle. |
| [IWICImagingFactory::CreateBitmapFromMemory](..\wincodec\nf-wincodec-iwicimagingfactory-createbitmapfrommemory.md) | Creates an IWICBitmap from a memory block. |
| [IWICImagingFactory::CreateBitmapFromSourceRect](..\wincodec\nf-wincodec-iwicimagingfactory-createbitmapfromsourcerect.md) | Creates an IWICBitmap from a specified rectangle of an IWICBitmapSource. |
| [IWICImagingFactory::CreateBitmapFromSource](..\wincodec\nf-wincodec-iwicimagingfactory-createbitmapfromsource.md) | Creates a IWICBitmap from a IWICBitmapSource. |
| [IWICImagingFactory::CreateBitmapScaler](..\wincodec\nf-wincodec-iwicimagingfactory-createbitmapscaler.md) | Creates a new instance of an IWICBitmapScaler. |
| [IWICImagingFactory::CreateBitmap](..\wincodec\nf-wincodec-iwicimagingfactory-createbitmap.md) | Creates an IWICBitmap object. |
| [IWICImagingFactory::CreateColorContext](..\wincodec\nf-wincodec-iwicimagingfactory-createcolorcontext.md) | Creates a new instance of the IWICColorContext class. |
| [IWICImagingFactory::CreateColorTransformer](..\wincodec\nf-wincodec-iwicimagingfactory-createcolortransformer.md) | Creates a new instance of the IWICColorTransform class. |
| [IWICImagingFactory::CreateComponentEnumerator](..\wincodec\nf-wincodec-iwicimagingfactory-createcomponentenumerator.md) | Creates an IEnumUnknown object of the specified component types. |
| [IWICImagingFactory::CreateComponentInfo](..\wincodec\nf-wincodec-iwicimagingfactory-createcomponentinfo.md) | Creates a new instance of the IWICComponentInfo class for the given component class identifier (CLSID). |
| [IWICImagingFactory::CreateDecoderFromFileHandle](..\wincodec\nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle.md) | Creates a new instance of the IWICBitmapDecoder based on the given file handle. |
| [IWICImagingFactory::CreateDecoderFromFilename](..\wincodec\nf-wincodec-iwicimagingfactory-createdecoderfromfilename.md) | Creates a new instance of the IWICBitmapDecoder class based on the given file. |
| [IWICImagingFactory::CreateDecoderFromStream](..\wincodec\nf-wincodec-iwicimagingfactory-createdecoderfromstream.md) | Creates a new instance of the IWICBitmapDecoder class based on the given IStream. |
| [IWICImagingFactory::CreateDecoder](..\wincodec\nf-wincodec-iwicimagingfactory-createdecoder.md) | Creates a new instance of IWICBitmapDecoder. |
| [IWICImagingFactory::CreateEncoder](..\wincodec\nf-wincodec-iwicimagingfactory-createencoder.md) | Creates a new instance of the IWICBitmapEncoder class. |
| [IWICImagingFactory::CreateFastMetadataEncoderFromDecoder](..\wincodec\nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder.md) | Creates a new instance of the fast metadata encoder based on the given IWICBitmapDecoder. |
| [IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode](..\wincodec\nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode.md) | Creates a new instance of the fast metadata encoder based on the given image frame. |
| [IWICImagingFactory::CreateFormatConverter](..\wincodec\nf-wincodec-iwicimagingfactory-createformatconverter.md) | Creates a new instance of the IWICFormatConverter class. |
| [IWICImagingFactory::CreatePalette](..\wincodec\nf-wincodec-iwicimagingfactory-createpalette.md) | Creates a new instance of the IWICPalette class. |
| [IWICImagingFactory::CreateQueryWriterFromReader](..\wincodec\nf-wincodec-iwicimagingfactory-createquerywriterfromreader.md) | Creates a new instance of a query writer based on the given query reader. The query writer will be pre-populated with metadata from the query reader. |
| [IWICImagingFactory::CreateQueryWriter](..\wincodec\nf-wincodec-iwicimagingfactory-createquerywriter.md) | Creates a new instance of a query writer. |
| [IWICImagingFactory::CreateStream](..\wincodec\nf-wincodec-iwicimagingfactory-createstream.md) | Creates a new instance of the IWICStream class. |
| [IWICJpegFrameDecode::ClearIndexing](..\wincodec\nf-wincodec-iwicjpegframedecode-clearindexing.md) | Removes the indexing from a JPEG that has been indexed using IWICJpegFrameDecode |
| [IWICJpegFrameDecode::CopyScan](..\wincodec\nf-wincodec-iwicjpegframedecode-copyscan.md) | Retrieves a copy of the compressed JPEG scan directly from the WIC decoder frame's output stream. |
| [IWICJpegFrameDecode::DoesSupportIndexing](..\wincodec\nf-wincodec-iwicjpegframedecode-doessupportindexing.md) | Retrieves a value indicating whether this decoder supports indexing for efficient random access. |
| [IWICJpegFrameDecode::GetAcHuffmanTable](..\wincodec\nf-wincodec-iwicjpegframedecode-getachuffmantable.md) | Retrieves a copy of the AC Huffman table for the specified scan and table. |
| [IWICJpegFrameDecode::GetDcHuffmanTable](..\wincodec\nf-wincodec-iwicjpegframedecode-getdchuffmantable.md) | Retrieves a copy of the DC Huffman table for the specified scan and table. |
| [IWICJpegFrameDecode::GetFrameHeader](..\wincodec\nf-wincodec-iwicjpegframedecode-getframeheader.md) | Retrieves header data from the entire frame. |
| [IWICJpegFrameDecode::GetQuantizationTable](..\wincodec\nf-wincodec-iwicjpegframedecode-getquantizationtable.md) | Retrieves a copy of the quantization table. |
| [IWICJpegFrameDecode::GetScanHeader](..\wincodec\nf-wincodec-iwicjpegframedecode-getscanheader.md) | Retrieves parameters from the Start Of Scan (SOS) marker for the scan with the specified index. |
| [IWICJpegFrameDecode::SetIndexing](..\wincodec\nf-wincodec-iwicjpegframedecode-setindexing.md) | Enables indexing of the JPEG for efficient random access. |
| [IWICJpegFrameEncode::GetAcHuffmanTable](..\wincodec\nf-wincodec-iwicjpegframeencode-getachuffmantable.md) | Retrieves a copy of the AC Huffman table for the specified scan and table. |
| [IWICJpegFrameEncode::GetDcHuffmanTable](..\wincodec\nf-wincodec-iwicjpegframeencode-getdchuffmantable.md) | Retrieves a copy of the DC Huffman table for the specified scan and table. |
| [IWICJpegFrameEncode::GetQuantizationTable](..\wincodec\nf-wincodec-iwicjpegframeencode-getquantizationtable.md) | Retrieves a copy of the quantization table. |
| [IWICJpegFrameEncode::WriteScan](..\wincodec\nf-wincodec-iwicjpegframeencode-writescan.md) | Writes scan data to a JPEG frame. |
| [IWICMetadataBlockReader::GetContainerFormat](..\wincodecsdk\nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat.md) | Retrieves the container format of the decoder. |
| [IWICMetadataBlockReader::GetCount](..\wincodecsdk\nf-wincodecsdk-iwicmetadatablockreader-getcount.md) | Retrieves the number of top level metadata blocks. |
| [IWICMetadataBlockReader::GetEnumerator](..\wincodecsdk\nf-wincodecsdk-iwicmetadatablockreader-getenumerator.md) | Retrieves an enumeration of IWICMetadataReader objects representing each of the top level metadata blocks. |
| [IWICMetadataBlockReader::GetReaderByIndex](..\wincodecsdk\nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex.md) | Retrieves an IWICMetadataReader for a specified top level metadata block. |
| [IWICMetadataBlockWriter::AddWriter](..\wincodecsdk\nf-wincodecsdk-iwicmetadatablockwriter-addwriter.md) | Adds a top-level metadata block by adding a IWICMetadataWriter for it. |
| [IWICMetadataBlockWriter::GetWriterByIndex](..\wincodecsdk\nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex.md) | Retrieves the IWICMetadataWriter that resides at the specified index. |
| [IWICMetadataBlockWriter::InitializeFromBlockReader](..\wincodecsdk\nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader.md) | Initializes an IWICMetadataBlockWriter from the given IWICMetadataBlockReader. This will prepopulate the metadata block writer with all the metadata in the metadata block reader. |
| [IWICMetadataBlockWriter::RemoveWriterByIndex](..\wincodecsdk\nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex.md) | Removes the metadata writer from the specified index location. |
| [IWICMetadataBlockWriter::SetWriterByIndex](..\wincodecsdk\nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex.md) | Replaces the metadata writer at the specified index location. |
| [IWICMetadataHandlerInfo::DoesRequireFixedSize](..\wincodecsdk\nf-wincodecsdk-iwicmetadatahandlerinfo-doesrequirefixedsize.md) | Determines if the metadata handler requires a fixed size. |
| [IWICMetadataHandlerInfo::DoesRequireFullStream](..\wincodecsdk\nf-wincodecsdk-iwicmetadatahandlerinfo-doesrequirefullstream.md) | Determines if the handler requires a full stream. |
| [IWICMetadataHandlerInfo::DoesSupportPadding](..\wincodecsdk\nf-wincodecsdk-iwicmetadatahandlerinfo-doessupportpadding.md) | Determines if the metadata handler supports padding. |
| [IWICMetadataHandlerInfo::GetContainerFormats](..\wincodecsdk\nf-wincodecsdk-iwicmetadatahandlerinfo-getcontainerformats.md) | Retrieves the container formats supported by the metadata handler. |
| [IWICMetadataHandlerInfo::GetDeviceManufacturer](..\wincodecsdk\nf-wincodecsdk-iwicmetadatahandlerinfo-getdevicemanufacturer.md) | Retrieves the device manufacturer of the metadata handler. |
| [IWICMetadataHandlerInfo::GetDeviceModels](..\wincodecsdk\nf-wincodecsdk-iwicmetadatahandlerinfo-getdevicemodels.md) | Retrieves the device models that support the metadata handler. |
| [IWICMetadataHandlerInfo::GetMetadataFormat](..\wincodecsdk\nf-wincodecsdk-iwicmetadatahandlerinfo-getmetadataformat.md) | Retrieves the metadata format of the metadata handler. |
| [IWICMetadataQueryReader::GetContainerFormat](..\wincodec\nf-wincodec-iwicmetadataqueryreader-getcontainerformat.md) | Gets the metadata query readers container format. |
| [IWICMetadataQueryReader::GetEnumerator](..\wincodec\nf-wincodec-iwicmetadataqueryreader-getenumerator.md) | Gets an enumerator of all metadata items at the current relative location within the metadata hierarchy. |
| [IWICMetadataQueryReader::GetLocation](..\wincodec\nf-wincodec-iwicmetadataqueryreader-getlocation.md) | Retrieves the current path relative to the root metadata block. |
| [IWICMetadataQueryReader::GetMetadataByName](..\wincodec\nf-wincodec-iwicmetadataqueryreader-getmetadatabyname.md) | Retrieves the metadata block or item identified by a metadata query expression. |
| [IWICMetadataQueryWriter::RemoveMetadataByName](..\wincodec\nf-wincodec-iwicmetadataquerywriter-removemetadatabyname.md) | Removes a metadata item from a specific location using a metadata query expression. |
| [IWICMetadataQueryWriter::SetMetadataByName](..\wincodec\nf-wincodec-iwicmetadataquerywriter-setmetadatabyname.md) | Sets a metadata item to a specific location. |
| [IWICMetadataReader::GetCount](..\wincodecsdk\nf-wincodecsdk-iwicmetadatareader-getcount.md) | Gets the number of metadata items within the reader. |
| [IWICMetadataReader::GetEnumerator](..\wincodecsdk\nf-wincodecsdk-iwicmetadatareader-getenumerator.md) | Gets an enumerator of all the metadata items. |
| [IWICMetadataReader::GetMetadataFormat](..\wincodecsdk\nf-wincodecsdk-iwicmetadatareader-getmetadataformat.md) | Gets the metadata format associated with the reader. |
| [IWICMetadataReader::GetMetadataHandlerInfo](..\wincodecsdk\nf-wincodecsdk-iwicmetadatareader-getmetadatahandlerinfo.md) | Gets the metadata handler info associated with the reader. |
| [IWICMetadataReader::GetValueByIndex](..\wincodecsdk\nf-wincodecsdk-iwicmetadatareader-getvaluebyindex.md) | Gets the metadata item at the given index. |
| [IWICMetadataReader::GetValue](..\wincodecsdk\nf-wincodecsdk-iwicmetadatareader-getvalue.md) | Gets the metadata item value. |
| [IWICMetadataReaderInfo::CreateInstance](..\wincodecsdk\nf-wincodecsdk-iwicmetadatareaderinfo-createinstance.md) | Creates an instance of an IWICMetadataReader. |
| [IWICMetadataReaderInfo::GetPatterns](..\wincodecsdk\nf-wincodecsdk-iwicmetadatareaderinfo-getpatterns.md) | Gets the metadata patterns associated with the metadata reader. |
| [IWICMetadataReaderInfo::MatchesPattern](..\wincodecsdk\nf-wincodecsdk-iwicmetadatareaderinfo-matchespattern.md) | Determines if a stream contains a metadata item pattern. |
| [IWICMetadataWriter::RemoveValueByIndex](..\wincodecsdk\nf-wincodecsdk-iwicmetadatawriter-removevaluebyindex.md) | Removes the metadata item at the specified index. |
| [IWICMetadataWriter::RemoveValue](..\wincodecsdk\nf-wincodecsdk-iwicmetadatawriter-removevalue.md) | Removes the metadata item that matches the given parameters. |
| [IWICMetadataWriter::SetValueByIndex](..\wincodecsdk\nf-wincodecsdk-iwicmetadatawriter-setvaluebyindex.md) | Sets the metadata item to the specified index. |
| [IWICMetadataWriter::SetValue](..\wincodecsdk\nf-wincodecsdk-iwicmetadatawriter-setvalue.md) | Sets the given metadata item. |
| [IWICMetadataWriterInfo::CreateInstance](..\wincodecsdk\nf-wincodecsdk-iwicmetadatawriterinfo-createinstance.md) | Creates an instance of an IWICMetadataWriter. |
| [IWICMetadataWriterInfo::GetHeader](..\wincodecsdk\nf-wincodecsdk-iwicmetadatawriterinfo-getheader.md) | Gets the metadata header for the metadata writer. |
| [IWICPalette::GetColorCount](..\wincodec\nf-wincodec-iwicpalette-getcolorcount.md) | Retrieves the number of colors in the color table. |
| [IWICPalette::GetColors](..\wincodec\nf-wincodec-iwicpalette-getcolors.md) | Fills out the supplied color array with the colors from the internal color table. The color array should be sized according to the return results from GetColorCount. |
| [IWICPalette::GetType](..\wincodec\nf-wincodec-iwicpalette-gettype.md) | Retrieves the WICBitmapPaletteType that describes the palette. |
| [IWICPalette::HasAlpha](..\wincodec\nf-wincodec-iwicpalette-hasalpha.md) | Indicates whether the palette contains an entry that is non-opaque (that is, an entry with an alpha that is less than 1). |
| [IWICPalette::InitializeCustom](..\wincodec\nf-wincodec-iwicpalette-initializecustom.md) | Initializes a palette to the custom color entries provided. |
| [IWICPalette::InitializeFromBitmap](..\wincodec\nf-wincodec-iwicpalette-initializefrombitmap.md) | Initializes a palette using a computed optimized values based on the reference bitmap. |
| [IWICPalette::InitializeFromPalette](..\wincodec\nf-wincodec-iwicpalette-initializefrompalette.md) | Initialize the palette based on a given palette. |
| [IWICPalette::InitializePredefined](..\wincodec\nf-wincodec-iwicpalette-initializepredefined.md) | Initializes the palette to one of the pre-defined palettes specified by WICBitmapPaletteType and optionally adds a transparent color. |
| [IWICPalette::IsBlackWhite](..\wincodec\nf-wincodec-iwicpalette-isblackwhite.md) | Retrieves a value that describes whether the palette is black and white. |
| [IWICPalette::IsGrayscale](..\wincodec\nf-wincodec-iwicpalette-isgrayscale.md) | Retrieves a value that describes whether a palette is grayscale. |
| [IWICPersistStream::LoadEx](..\wincodecsdk\nf-wincodecsdk-iwicpersiststream-loadex.md) | Loads data from an input stream using the given parameters. |
| [IWICPersistStream::SaveEx](..\wincodecsdk\nf-wincodecsdk-iwicpersiststream-saveex.md) | Saves the IWICPersistStream to the given input IStream using the given parameters. |
| [IWICPixelFormatInfo2::GetNumericRepresentation](..\wincodec\nf-wincodec-iwicpixelformatinfo2-getnumericrepresentation.md) | IWICPixelFormatInfo2 |
| [IWICPixelFormatInfo2::SupportsTransparency](..\wincodec\nf-wincodec-iwicpixelformatinfo2-supportstransparency.md) | Returns whether the format supports transparent pixels. |
| [IWICPixelFormatInfo::GetBitsPerPixel](..\wincodec\nf-wincodec-iwicpixelformatinfo-getbitsperpixel.md) | Gets the bits per pixel (BPP) of the pixel format. |
| [IWICPixelFormatInfo::GetChannelCount](..\wincodec\nf-wincodec-iwicpixelformatinfo-getchannelcount.md) | Gets the number of channels the pixel format contains. |
| [IWICPixelFormatInfo::GetChannelMask](..\wincodec\nf-wincodec-iwicpixelformatinfo-getchannelmask.md) | Gets the pixel format's channel mask. |
| [IWICPixelFormatInfo::GetColorContext](..\wincodec\nf-wincodec-iwicpixelformatinfo-getcolorcontext.md) | Gets the pixel format's IWICColorContext. |
| [IWICPixelFormatInfo::GetFormatGUID](..\wincodec\nf-wincodec-iwicpixelformatinfo-getformatguid.md) | Gets the pixel format GUID. |
| [IWICPlanarBitmapFrameEncode::WritePixels](..\wincodec\nf-wincodec-iwicplanarbitmapframeencode-writepixels.md) | Writes lines from the source planes to the encoded format. |
| [IWICPlanarBitmapFrameEncode::WriteSource](..\wincodec\nf-wincodec-iwicplanarbitmapframeencode-writesource.md) | Writes lines from the source planes to the encoded format. |
| [IWICPlanarBitmapSourceTransform::CopyPixels](..\wincodec\nf-wincodec-iwicplanarbitmapsourcetransform-copypixels.md) | Copies pixels into the destination planes. Configured by the supplied input parameters. |
| [IWICPlanarBitmapSourceTransform::DoesSupportTransform](..\wincodec\nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform.md) | Use this method to determine if a desired planar output is supported and allow the caller to choose an optimized code path if it is. |
| [IWICPlanarFormatConverter::CanConvert](..\wincodec\nf-wincodec-iwicplanarformatconverter-canconvert.md) | Query if the format converter can convert from one format to another. |
| [IWICPlanarFormatConverter::Initialize](..\wincodec\nf-wincodec-iwicplanarformatconverter-initialize.md) | Initializes a format converter with a planar source, and specifies the interleaved output pixel format. |
| [IWICProgressCallback::Notify](..\wincodec\nf-wincodec-iwicprogresscallback-notify.md) | Notify method is documented only for compliance; its use is not recommended and may be altered or unavailable in the future. Instead, and use RegisterProgressNotification. |
| [IWICProgressiveLevelControl::GetCurrentLevel](..\wincodec\nf-wincodec-iwicprogressivelevelcontrol-getcurrentlevel.md) | Gets the decoder's current progressive level. |
| [IWICProgressiveLevelControl::GetLevelCount](..\wincodec\nf-wincodec-iwicprogressivelevelcontrol-getlevelcount.md) | Gets the number of levels of progressive decoding supported by the CODEC. |
| [IWICProgressiveLevelControl::SetCurrentLevel](..\wincodec\nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel.md) | Specifies the level to retrieve on the next call to CopyPixels. |
| [IWICStream::InitializeFromFilename](..\wincodec\nf-wincodec-iwicstream-initializefromfilename.md) | Initializes a stream from a particular file. |
| [IWICStream::InitializeFromIStreamRegion](..\wincodec\nf-wincodec-iwicstream-initializefromistreamregion.md) | Initializes the stream as a substream of another stream. |
| [IWICStream::InitializeFromIStream](..\wincodec\nf-wincodec-iwicstream-initializefromistream.md) | Initializes a stream from another stream. Access rights are inherited from the underlying stream. |
| [IWICStream::InitializeFromMemory](..\wincodec\nf-wincodec-iwicstream-initializefrommemory.md) | Initializes a stream to treat a block of memory as a stream. The stream cannot grow beyond the buffer size. |
| [IWICStreamProvider::GetPersistOptions](..\wincodecsdk\nf-wincodecsdk-iwicstreamprovider-getpersistoptions.md) | Gets the persist options used when initializing the component with a stream. |
| [IWICStreamProvider::GetPreferredVendorGUID](..\wincodecsdk\nf-wincodecsdk-iwicstreamprovider-getpreferredvendorguid.md) | Gets the preferred vendor GUID. |
| [IWICStreamProvider::GetStream](..\wincodecsdk\nf-wincodecsdk-iwicstreamprovider-getstream.md) | Gets the stream held by the component. |
| [IWICStreamProvider::RefreshStream](..\wincodecsdk\nf-wincodecsdk-iwicstreamprovider-refreshstream.md) | Informs the component that the content of the stream it's holding onto may have changed. The component should respond by dirtying any cached information from the stream. |
