---
UID: TP:gdiplus
ms.assetid: 7cb49be5-6f39-391f-a093-c2e9fa92c4fc
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# GDI+



Overview of the GDI+ technology.

To develop GDI+, you need these headers:

 * [gdiplusbase.h](..\gdiplusbase\index.md)
 * [gdiplusbrush.h](..\gdiplusbrush\index.md)
 * [gdipluscolor.h](..\gdipluscolor\index.md)
 * [gdipluscolormatrix.h](..\gdipluscolormatrix\index.md)
 * [gdipluseffects.h](..\gdipluseffects\index.md)
 * [gdiplusenums.h](..\gdiplusenums\index.md)
 * [gdiplusgraphics.h](..\gdiplusgraphics\index.md)
 * [gdiplusheaders.h](..\gdiplusheaders\index.md)
 * [gdiplusimageattributes.h](..\gdiplusimageattributes\index.md)
 * [gdiplusimagecodec.h](..\gdiplusimagecodec\index.md)
 * [gdiplusimaging.h](..\gdiplusimaging\index.md)
 * [gdiplusinit.h](..\gdiplusinit\index.md)
 * [gdipluslinecaps.h](..\gdipluslinecaps\index.md)
 * [gdiplusmatrix.h](..\gdiplusmatrix\index.md)
 * [gdiplusmetaheader.h](..\gdiplusmetaheader\index.md)
 * [gdipluspath.h](..\gdipluspath\index.md)
 * [gdipluspen.h](..\gdipluspen\index.md)
 * [gdipluspixelformats.h](..\gdipluspixelformats\index.md)
 * [gdiplusstringformat.h](..\gdiplusstringformat\index.md)
 * [gdiplustypes.h](..\gdiplustypes\index.md)

For the programming guide, see [GDI+](https://review.docs.microsoft.com/en-us/win32-test/gdiplus).

## Functions

| Title   | Description   |
| ---- |:---- |
| [GdiplusShutdown function](..\gdiplusinit\nf-gdiplusinit-gdiplusshutdown.md) | The GdiplusShutdown function cleans up resources used by Windows GDI+. Each call to GdiplusStartup should be paired with a call to GdiplusShutdown. |
| [GdiplusStartup function](..\gdiplusinit\nf-gdiplusinit-gdiplusstartup.md) | The GdiplusStartup function initializes Windows GDI+. Call GdiplusStartup before making any other GDI+ calls, and call GdiplusShutdown when you have finished using GDI+. |
| [GetImageDecoders function](..\gdiplusimagecodec\nf-gdiplusimagecodec-getimagedecoders.md) | The GetImageDecoders function gets an array of ImageCodecInfo objects that contain information about the available image decoders. |
| [GetImageDecodersSize function](..\gdiplusimagecodec\nf-gdiplusimagecodec-getimagedecoderssize.md) | The GetImageDecodersSize function gets the number of available image decoders and the total size of the array of ImageCodecInfo objects that is returned by the GetImageDecoders function. |
| [GetImageEncoders function](..\gdiplusimagecodec\nf-gdiplusimagecodec-getimageencoders.md) | The GetImageEncoders function gets an array of ImageCodecInfo objects that contain information about the available image encoders. |
| [GetImageEncodersSize function](..\gdiplusimagecodec\nf-gdiplusimagecodec-getimageencoderssize.md) | The GetImageEncodersSize function gets the number of available image encoders and the total size of the array of ImageCodecInfo objects that is returned by the GetImageEncoders function. |
| [GetPixelFormatSize function](..\gdipluspixelformats\nf-gdipluspixelformats-getpixelformatsize.md) | The GetPixelFormatSize method returns the number of bits per pixel used by a specified pixel format. |
| [IsAlphaPixelFormat function](..\gdipluspixelformats\nf-gdipluspixelformats-isalphapixelformat.md) | The IsAlphaPixelFormat method determines whether a specified pixel format has an alpha component. |
| [IsCanonicalPixelFormat function](..\gdipluspixelformats\nf-gdipluspixelformats-iscanonicalpixelformat.md) | The IsCanonicalPixelFormat method determines whether a specified pixel format is one of the canonical formats |
| [IsExtendedPixelFormat function](..\gdipluspixelformats\nf-gdipluspixelformats-isextendedpixelformat.md) | The IsExtendedPixelFormat method determines whether a specified pixel format uses 16 bits per color channel. |
| [IsIndexedPixelFormat function](..\gdipluspixelformats\nf-gdipluspixelformats-isindexedpixelformat.md) | The IsIndexedPixelFormat method determines whether a specified pixel format is an indexed format. |
| [ObjectTypeIsValid function](..\gdiplusenums\nf-gdiplusenums-objecttypeisvalid.md) | The ObjectTypeIsValid function determines whether an element of the ObjectType enumeration represents a valid object type. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [BlurParams structure](..\gdipluseffects\ns-gdipluseffects-blurparams.md) | A BlurParams structure contains members that specify the nature of a Gaussian blur. |
| [BrightnessContrastParams structure](..\gdipluseffects\ns-gdipluseffects-brightnesscontrastparams.md) | A BlurParams structure contains members that specify the nature of a Gaussian blur. |
| [ColorBalanceParams structure](..\gdipluseffects\ns-gdipluseffects-colorbalanceparams.md) | A ColorBalanceParams structure contains members that specify the nature of a color balance adjustment. |
| [ColorCurveParams structure](..\gdipluseffects\ns-gdipluseffects-colorcurveparams.md) | A ColorCurveParams structure contains members that specify an adjustment to the colors of a bitmap. |
| [ColorLUTParams structure](..\gdipluseffects\ns-gdipluseffects-colorlutparams.md) | A ColorLUTParams structure contains members (color lookup tables) that specify color adjustments to a bitmap. |
| [ColorMap structure](..\gdipluscolormatrix\ns-gdipluscolormatrix-colormap.md) | The ColorMap structure contains two Color objects. Several methods of the ImageAttributes class adjust image colors by using a color remap table, which is an array of ColorMap structures. |
| [ColorMatrix structure](..\gdipluscolormatrix\ns-gdipluscolormatrix-colormatrix.md) | The ColorMatrix structure contains a 5&#215;5 matrix of real numbers. Several methods of the ImageAttributes class adjust image colors by using a color matrix. |
| [ColorPalette structure](..\gdipluspixelformats\ns-gdipluspixelformats-colorpalette.md) | The ColorPalette structure defines an array of colors that make up a color palette. The colors are 32-bit ARGB colors. |
| [ENHMETAHEADER3 structure](..\gdiplusmetaheader\ns-gdiplusmetaheader-enhmetaheader3.md) | The ENHMETAHEADER3 structure contains enhanced-metafile data including the dimensions of the metafile image, the number of records in the metafile, and the resolution of the device on which the metafile was created. |
| [GdiplusAbort structure](..\gdiplustypes\ns-gdiplustypes-gdiplusabort.md) | The GdiplusAbort structure provides a mechanism that allows Windows GDI+ to call an application-defined Abort method periodically during time-consuming rendering operations. |
| [GdiplusStartupInput structure](..\gdiplusinit\ns-gdiplusinit-gdiplusstartupinput.md) | The GdiplusStartupInput structure holds a block of arguments that are required by the GdiplusStartup function. |
| [GdiplusStartupOutput structure](..\gdiplusinit\ns-gdiplusinit-gdiplusstartupoutput.md) | The GdiplusStartup function uses the GdiplusStartupOutput structure to return (in its output parameter) a pointer to a hook function and a pointer to an unhook function. |
| [HueSaturationLightnessParams structure](..\gdipluseffects\ns-gdipluseffects-huesaturationlightnessparams.md) | The HueSaturationLightnessParams structure contains members that specify hue, saturation and lightness adjustments to a bitmap. |
| [LevelsParams structure](..\gdipluseffects\ns-gdipluseffects-levelsparams.md) | The LevelsParams structure contains members that specify adjustments to the light, midtone, or dark areas of a bitmap. |
| [PWMFRect16 structure](..\gdiplusmetaheader\ns-gdiplusmetaheader-pwmfrect16.md) | The PWMFRect16 structure defines a rectangle that bounds a placeable metafile. The rectangle defines the size and position of the metafile. |
| [RedEyeCorrectionParams structure](..\gdipluseffects\ns-gdipluseffects-redeyecorrectionparams.md) | A RedEyeCorrectionParams structure contains members that specify the areas of a bitmap to which a red-eye correction is applied. |
| [SharpenParams structure](..\gdipluseffects\ns-gdipluseffects-sharpenparams.md) | The SharpenParams structure contains members that specify the nature of a sharpening adjustment to a bitmap. |
| [TintParams structure](..\gdipluseffects\ns-gdipluseffects-tintparams.md) | A TintParams structure contains members that specify the nature of a tint adjustment to a bitmap. |
| [WmfPlaceableFileHeader structure](..\gdiplusmetaheader\ns-gdiplusmetaheader-wmfplaceablefileheader.md) | The WmfPlaceableFileHeader structure defines the fields of a placeable metafile header. Placeable metafiles were created as a way of specifying how a metafile is mapped and scaled on a display device. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [BrushType enumeration](..\gdiplusenums\ne-gdiplusenums-brushtype.md) | The BrushType enumeration indicates the type of brush. There are five types of brushes. |
| [ColorAdjustType enumeration](..\gdipluscolormatrix\ne-gdipluscolormatrix-coloradjusttype.md) | The ColorAdjustType enumeration specifies which GDI+ objects use color-adjustment information. |
| [ColorChannelFlags enumeration](..\gdipluscolor\ne-gdipluscolor-colorchannelflags.md) | The ColorChannelFlags enumeration specifies individual channels in the CMYK (cyan, magenta, yellow, black) color space. This enumeration is used by the ImageAttributes |
| [ColorMatrixFlags enumeration](..\gdipluscolormatrix\ne-gdipluscolormatrix-colormatrixflags.md) | The ColorMatrixFlags enumeration specifies the types of images and colors that will be affected by the color and grayscale adjustment settings of an ImageAttributes object. |
| [CombineMode enumeration](..\gdiplusenums\ne-gdiplusenums-combinemode.md) | The CombineMode enumeration specifies how a new region is combined with an existing region. |
| [CompositingMode enumeration](..\gdiplusenums\ne-gdiplusenums-compositingmode.md) | The CompositingMode enumeration specifies how rendered colors are combined with background colors. This enumeration is used by the Graphics |
| [CompositingQuality enumeration](..\gdiplusenums\ne-gdiplusenums-compositingquality.md) | The CompositingQuality enumeration specifies whether gamma correction is applied when colors are blended with background colors. |
| [CoordinateSpace enumeration](..\gdiplusenums\ne-gdiplusenums-coordinatespace.md) | The CoordinateSpace enumeration specifies coordinate spaces. |
| [CurveAdjustments enumeration](..\gdipluseffects\ne-gdipluseffects-curveadjustments.md) | The ColorCurve class encompasses the eight bitmap adjustments listed in the CurveAdjustments enumeration. |
| [CurveChannel enumeration](..\gdipluseffects\ne-gdipluseffects-curvechannel.md) | The CurveChannel enumeration specifies which color channels are affected by a ColorCurve bitmap adjustment. |
| [DashCap enumeration](..\gdiplusenums\ne-gdiplusenums-dashcap.md) | The DashCap enumeration specifies the type of graphic shape to use on both ends of each dash in a dashed line. |
| [DashStyle enumeration](..\gdiplusenums\ne-gdiplusenums-dashstyle.md) | The DashStyle enumeration specifies the line style of a line drawn with a Windows GDI+ pen. The line can be drawn by using one of several predefined styles or a custom style. |
| [DriverStringOptions enumeration](..\gdiplusenums\ne-gdiplusenums-driverstringoptions.md) | The DriverStringOptions enumeration specifies the spacing, orientation, and quality of the rendering for driver strings. |
| [EmfPlusRecordType enumeration](..\gdiplusenums\ne-gdiplusenums-emfplusrecordtype.md) | The EmfPlusRecordType enumeration identifies metafile record types used in Windows Metafile Format (WMF), Enhanced Metafile (EMF), and EMF+ files. The elements of the EmfPlusRecordType enumeration come in three groups. |
| [EmfToWmfBitsFlags enumeration](..\gdiplusenums\ne-gdiplusenums-emftowmfbitsflags.md) | Specifies options for the Metafile |
| [EmfType enumeration](..\gdiplusenums\ne-gdiplusenums-emftype.md) | The EmfType enumeration specifies the nature of the records that are placed in an Enhanced Metafile (EMF) file. This enumeration is used by several constructors in the Metafile class. |
| [EncoderParameterValueType enumeration](..\gdiplusenums\ne-gdiplusenums-encoderparametervaluetype.md) | The EncoderParameterValueType enumeration specifies data types for image codec (encoder/decoder) parameters. An element of this enumeration is assigned to the Type data member of an EncoderParameter object. |
| [EncoderValue enumeration](..\gdiplusenums\ne-gdiplusenums-encodervalue.md) | The EncoderValue enumeration specifies values that can be passed as arguments to image encoders. For more information about image encoders, see Using Image Encoders and Decoders . |
| [FillMode enumeration](..\gdiplusenums\ne-gdiplusenums-fillmode.md) | The FillMode enumeration specifies how to fill areas that are formed when a path or curve intersects itself. |
| [FlushIntention enumeration](..\gdiplusenums\ne-gdiplusenums-flushintention.md) | The FlushIntention enumeration specifies when to flush the queue of graphics operations. |
| [FontStyle enumeration](..\gdiplusenums\ne-gdiplusenums-fontstyle.md) | The FontStyle enumeration specifies the style of the typeface of a font. Styles can be combined. |
| [HatchStyle enumeration](..\gdiplusenums\ne-gdiplusenums-hatchstyle.md) | The HatchStyle enumeration specifies the hatch pattern used by a brush of type HatchBrush. The hatch pattern consists of a solid background color and lines drawn over the background. |
| [HistogramFormat enumeration](..\gdipluscolormatrix\ne-gdipluscolormatrix-histogramformat.md) | The HistogramFormat enumeration specifies the number and type of histograms that represent the color channels of a bitmap. This enumeration is used with the Bitmap |
| [HotkeyPrefix enumeration](..\gdiplusenums\ne-gdiplusenums-hotkeyprefix.md) | The HotkeyPrefix enumeration specifies how to display hot keys. There are three options |
| [ImageCodecFlags enumeration](..\gdiplusimaging\ne-gdiplusimaging-imagecodecflags.md) | The ImageCodecFlags enumeration indicates attributes of an image codec. |
| [ImageFlags enumeration](..\gdiplusimaging\ne-gdiplusimaging-imageflags.md) | The ImageFlags enumeration specifies the attributes of the pixel data contained in an Image object. The Image |
| [ImageLockMode enumeration](..\gdiplusimaging\ne-gdiplusimaging-imagelockmode.md) | The ImageLockMode enumeration specifies flags that are passed to the flags parameter of the Bitmap |
| [ImageType enumeration](..\gdiplusenums\ne-gdiplusenums-imagetype.md) | The ImageType enumeration indicates whether an image is a bitmap or a metafile. The Image |
| [InterpolationMode enumeration](..\gdiplusenums\ne-gdiplusenums-interpolationmode.md) | The InterpolationMode enumeration specifies the algorithm that is used when images are scaled or rotated. This enumeration is used by the Graphics |
| [ItemDataPosition enumeration](..\gdiplusimaging\ne-gdiplusimaging-itemdataposition.md) | The ItemDataPosition enumeration is used to specify the location of custom metadata in an image file. |
| [LineCap enumeration](..\gdiplusenums\ne-gdiplusenums-linecap.md) | The LineCap enumeration specifies the type of graphic shape to use on the end of a line drawn with a Windows GDI+ pen. |
| [LineJoin enumeration](..\gdiplusenums\ne-gdiplusenums-linejoin.md) | The LineJoin enumeration specifies how to join two lines that are drawn by the same pen and whose ends meet. At the intersection of the two line ends, a line join makes the join look more continuous. |
| [LinearGradientMode enumeration](..\gdiplusenums\ne-gdiplusenums-lineargradientmode.md) | The LinearGradientMode enumeration specifies the direction in which the change of color occurs for a linear gradient brush. |
| [MatrixOrder enumeration](..\gdiplusenums\ne-gdiplusenums-matrixorder.md) | The MatrixOrder enumeration specifies the order of multiplication when a new matrix is multiplied by an existing matrix. |
| [MetafileFrameUnit enumeration](..\gdiplusenums\ne-gdiplusenums-metafileframeunit.md) | The MetafileFrameUnit enumeration specifies the unit of measure for a metafile frame rectangle. |
| [MetafileType enumeration](..\gdiplusenums\ne-gdiplusenums-metafiletype.md) | The MetafileType enumeration specifies types of metafiles. The MetafileHeader |
| [ObjectType enumeration](..\gdiplusenums\ne-gdiplusenums-objecttype.md) | The ObjectType enumeration indicates the object type value of an EMF+ record. |
| [PaletteFlags enumeration](..\gdipluspixelformats\ne-gdipluspixelformats-paletteflags.md) | The PaletteFlags enumeration indicates attributes of the color data in a palette. |
| [PaletteType enumeration](..\gdipluspixelformats\ne-gdipluspixelformats-palettetype.md) | The PaletteType enumeration is used by the Bitmap |
| [PathPointType enumeration](..\gdiplusenums\ne-gdiplusenums-pathpointtype.md) | The PathPointType enumeration indicates point types and flags for the data points in a path. |
| [PenAlignment enumeration](..\gdiplusenums\ne-gdiplusenums-penalignment.md) | The PenAlignment enumeration specifies the alignment of a pen relative to the stroke that is being drawn. |
| [PenType enumeration](..\gdiplusenums\ne-gdiplusenums-pentype.md) | The PenType enumeration indicates the type of pattern, texture, or gradient that a pen draws. |
| [PixelOffsetMode enumeration](..\gdiplusenums\ne-gdiplusenums-pixeloffsetmode.md) | The PixelOffsetMode enumeration specifies the pixel offset mode of a Graphics object. This enumeration is used by the Graphics |
| [RotateFlipType enumeration](..\gdiplusimaging\ne-gdiplusimaging-rotatefliptype.md) | The RotateFlipType enumeration specifies the direction of an image's rotation and the axis used to flip the image. |
| [SmoothingMode enumeration](..\gdiplusenums\ne-gdiplusenums-smoothingmode.md) | The SmoothingMode enumeration specifies the type of smoothing (antialiasing) that is applied to lines and curves. This enumeration is used by the Graphics |
| [Status enumeration](..\gdiplustypes\ne-gdiplustypes-status.md) | The Status enumeration indicates the result of a Windows GDI+ method call. |
| [StringAlignment enumeration](..\gdiplusenums\ne-gdiplusenums-stringalignment.md) | The StringAlignment enumeration specifies how a string is aligned in reference to the bounding rectangle. A bounding rectangle is used to define the area in which the text displays. |
| [StringDigitSubstitute enumeration](..\gdiplusenums\ne-gdiplusenums-stringdigitsubstitute.md) | The StringDigitSubstitute enumeration specifies how to substitute digits in a string according to a user's locale or language. |
| [StringFormatFlags enumeration](..\gdiplusenums\ne-gdiplusenums-stringformatflags.md) | The StringFormatFlags enumeration specifies text layout information (such as orientation and clipping) and display manipulations (such as ellipsis insertion, digit substitution, and representation of characters that are not supported by a font). |
| [StringTrimming enumeration](..\gdiplusenums\ne-gdiplusenums-stringtrimming.md) | The StringTrimming enumeration specifies how to trim characters from a string so that the string fits into a layout rectangle. The layout rectangle is used to position and size the display string. |
| [TextRenderingHint enumeration](..\gdiplusenums\ne-gdiplusenums-textrenderinghint.md) | The TextRenderingHint enumeration specifies the process used to render text. The process affects the quality of the text. |
| [Unit enumeration](..\gdiplusenums\ne-gdiplusenums-unit.md) | The Unit enumeration specifies the unit of measure for a given data type. |
| [WarpMode enumeration](..\gdiplusenums\ne-gdiplusenums-warpmode.md) | The WarpMode enumeration specifies warp modes that can be used to transform images. |
| [WrapMode enumeration](..\gdiplusenums\ne-gdiplusenums-wrapmode.md) | The WrapMode enumeration specifies how repeated copies of an image are used to tile an area. |

## Classes

| Title   | Description   |
| ---- |:---- |
| [AdjustableArrowCap class](..\gdipluslinecaps\nl-gdipluslinecaps-adjustablearrowcap.md) | The AdjustableArrowCap class is a subclass of the CustomLineCap. This class builds a line cap that looks like an arrow. |
| [BitmapData class](..\gdiplusimaging\nl-gdiplusimaging-bitmapdata.md) | The BitmapData class is used by the Bitmap |
| [BrightnessContrast class](..\gdipluseffects\nl-gdipluseffects-brightnesscontrast.md) | The BrightnessContrast class enables you to change the brightness and contrast of a bitmap. |
| [CharacterRange class](..\gdiplustypes\nl-gdiplustypes-characterrange.md) | A CharacterRange object specifies a range of character positions within a string. |
| [CharacterRange class](..\gdiplustypes\nl-gdiplustypes-characterrange~r1.md) | A CharacterRange object specifies a range of character positions within a string. |
| [ColorBalance class](..\gdipluseffects\nl-gdipluseffects-colorbalance.md) | The ColorBalance class enables you to change the color balance (relative amounts of red, green, and blue) of a bitmap. |
| [ColorCurve class](..\gdipluseffects\nl-gdipluseffects-colorcurve.md) | The ColorCurve class encompasses eight separate adjustments |
| [ColorLUT class](..\gdipluseffects\nl-gdipluseffects-colorlut.md) | A ColorLUTParams structure has four members, each being a lookup table for a particular color channel |
| [ColorMatrixEffect class](..\gdipluseffects\nl-gdipluseffects-colormatrixeffect.md) | The ColorMatrixEffect class enables you to apply an affine transformation to a bitmap. |
| [Effect class](..\gdipluseffects\nl-gdipluseffects-effect.md) | The Effect class serves as a base class for eleven classes that you can use to apply effects and adjustments to bitmaps. The following classes descend from Effect. |
| [EncoderParameter class](..\gdiplusimaging\nl-gdiplusimaging-encoderparameter.md) | An EncoderParameter object holds a parameter that can be passed to an image encoder. An EncoderParameter object can also be used to receive a list of possible values supported by a particular parameter of a particular image encoder. |
| [EncoderParameters class](..\gdiplusimaging\nl-gdiplusimaging-encoderparameters.md) | An EncoderParameters object is an array of EncoderParameter objects along with a data member that specifies the number of EncoderParameter objects in the array. |
| [GraphicsPathIterator class](..\gdipluspath\nl-gdipluspath-graphicspathiterator.md) | This GraphicsPathIterator class provides methods for isolating selected subsets of the path stored in a GraphicsPath object. |
| [GraphicsPathIterator class](..\gdipluspath\nl-gdipluspath-graphicspathiterator~r1.md) | This GraphicsPathIterator class provides methods for isolating selected subsets of the path stored in a GraphicsPath object. |
| [HueSaturationLightness class](..\gdipluseffects\nl-gdipluseffects-huesaturationlightness.md) | The HueSaturationLightness class enables you to change the hue, saturation, and lightness of a bitmap. |
| [ImageCodecInfo class](..\gdiplusimaging\nl-gdiplusimaging-imagecodecinfo.md) | An ImageCodecInfo object stores information about an image codec (encoder/decoder). |
| [ImageItemData class](..\gdiplusimaging\nl-gdiplusimaging-imageitemdata.md) | The ImageItemData class is used to store and retrieve custom image metadata. Windows GDI+ supports custom metadata for JPEG, PNG, and GIF image files. |
| [MetafileHeader class](..\gdiplusmetaheader\nl-gdiplusmetaheader-metafileheader.md) | A MetafileHeader object stores properties of an associated metafile. |
| [PropertyItem class](..\gdiplusimaging\nl-gdiplusimaging-propertyitem.md) | The PropertyItem class is a helper class for the Image and Bitmap classes. A PropertyItem object holds one piece of image metadata. |
| [RedEyeCorrection class](..\gdipluseffects\nl-gdipluseffects-redeyecorrection.md) | The RedEyeCorrection class enables you to correct the red eyes that sometimes occur in flash photographs. |
| [Sharpen class](..\gdipluseffects\nl-gdipluseffects-sharpen.md) | The Sharpen class enables you to adjust the sharpness of a bitmap. |
| [StringFormat class](..\gdiplusstringformat\nl-gdiplusstringformat-stringformat.md) | The StringFormat class encapsulates text layout information (such as alignment, orientation, tab stops, and clipping) and display manipulations (such as trimming, font substitution for characters that are not supported by the requested font, and digit substitution for languages that do not use Western European digits). A StringFormat object can be passed to the DrawString Methods method to format a string. |
| [Tint class](..\gdipluseffects\nl-gdipluseffects-tint.md) | The Tint class enables you to apply a tint to a bitmap. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [AdjustableArrowCap::AdjustableArrowCap(IN REAL,IN REAL,IN BOOL)](..\gdipluslinecaps\nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(in real,in real,in bool).md) | Creates an adjustable arrow line cap with the specified height and width. The arrow line cap can be filled or nonfilled. The middle inset defaults to zero. |
| [AdjustableArrowCap::AdjustableArrowCap(const AdjustableArrowCap &)](..\gdipluslinecaps\nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(const adjustablearrowcap &).md) | Creates an adjustable arrow line cap with the specified height and width. The arrow line cap can be filled or nonfilled. The middle inset defaults to zero. |
| [AdjustableArrowCap::GetHeight](..\gdipluslinecaps\nf-gdipluslinecaps-adjustablearrowcap-getheight.md) | The AdjustableArrowCap |
| [AdjustableArrowCap::GetMiddleInset](..\gdipluslinecaps\nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset.md) | The AdjustableArrowCap |
| [AdjustableArrowCap::GetWidth](..\gdipluslinecaps\nf-gdipluslinecaps-adjustablearrowcap-getwidth.md) | The AdjustableArrowCap |
| [AdjustableArrowCap::IsFilled](..\gdipluslinecaps\nf-gdipluslinecaps-adjustablearrowcap-isfilled.md) | The AdjustableArrowCap |
| [AdjustableArrowCap::SetFillState](..\gdipluslinecaps\nf-gdipluslinecaps-adjustablearrowcap-setfillstate.md) | The AdjustableArrowCap |
| [AdjustableArrowCap::SetHeight](..\gdipluslinecaps\nf-gdipluslinecaps-adjustablearrowcap-setheight.md) | The AdjustableArrowCap |
| [AdjustableArrowCap::SetMiddleInset](..\gdipluslinecaps\nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset.md) | The AdjustableArrowCap |
| [AdjustableArrowCap::SetWidth](..\gdipluslinecaps\nf-gdipluslinecaps-adjustablearrowcap-setwidth.md) | The AdjustableArrowCap |
| [Bitmap::FromBITMAPINFO](..\gdiplusheaders\nf-gdiplusheaders-bitmap-frombitmapinfo.md) | The Bitmap |
| [Bitmap::FromDirectDrawSurface7](..\gdiplusheaders\nf-gdiplusheaders-bitmap-fromdirectdrawsurface7.md) | The Bitmap |
| [Bitmap::FromFile](..\gdiplusheaders\nf-gdiplusheaders-bitmap-fromfile.md) | The Bitmap |
| [Bitmap::FromHBITMAP](..\gdiplusheaders\nf-gdiplusheaders-bitmap-fromhbitmap.md) | The Bitmap |
| [Bitmap::FromHICON](..\gdiplusheaders\nf-gdiplusheaders-bitmap-fromhicon.md) | The Bitmap |
| [Bitmap::FromResource](..\gdiplusheaders\nf-gdiplusheaders-bitmap-fromresource.md) | The Bitmap |
| [Bitmap::FromStream](..\gdiplusheaders\nf-gdiplusheaders-bitmap-fromstream.md) | The Bitmap |
| [Bitmap::GetHBITMAP](..\gdiplusheaders\nf-gdiplusheaders-bitmap-gethbitmap.md) | The Bitmap |
| [Bitmap::GetHICON](..\gdiplusheaders\nf-gdiplusheaders-bitmap-gethicon.md) | The Bitmap |
| [Bitmap::GetPixel](..\gdiplusheaders\nf-gdiplusheaders-bitmap-getpixel.md) | The Bitmap |
| [Bitmap::LockBits](..\gdiplusheaders\nf-gdiplusheaders-bitmap-lockbits.md) | The Bitmap |
| [Bitmap::SetPixel](..\gdiplusheaders\nf-gdiplusheaders-bitmap-setpixel.md) | The Bitmap |
| [Bitmap::SetResolution](..\gdiplusheaders\nf-gdiplusheaders-bitmap-setresolution.md) | The Bitmap |
| [Bitmap::UnlockBits](..\gdiplusheaders\nf-gdiplusheaders-bitmap-unlockbits.md) | The Bitmap |
| [Blur::Blur](..\gdipluseffects\nf-gdipluseffects-blur-blur.md) | Creates a Blur object. |
| [Blur::GetParameters](..\gdipluseffects\nf-gdipluseffects-blur-getparameters.md) | The Blur |
| [Blur::SetParameters](..\gdipluseffects\nf-gdipluseffects-blur-setparameters.md) | The Blur |
| [BrightnessContrast::BrightnessContrast](..\gdipluseffects\nf-gdipluseffects-brightnesscontrast-brightnesscontrast.md) | Creates a new BrightnessContrast object. |
| [BrightnessContrast::GetParameters](..\gdipluseffects\nf-gdipluseffects-brightnesscontrast-getparameters.md) | The BrightnessContrast |
| [BrightnessContrast::SetParameters](..\gdipluseffects\nf-gdipluseffects-brightnesscontrast-setparameters.md) | The BrightnessContrast |
| [Brush::Clone](..\gdiplusbrush\nf-gdiplusbrush-brush-clone.md) | The Brush |
| [Brush::GetLastStatus](..\gdiplusbrush\nf-gdiplusbrush-brush-getlaststatus.md) | The Brush |
| [Brush::GetType](..\gdiplusbrush\nf-gdiplusbrush-brush-gettype.md) | The Brush |
| [CachedBitmap::CachedBitmap(IN Bitmap,IN Graphics)](..\gdiplusheaders\nf-gdiplusheaders-cachedbitmap-cachedbitmap(in bitmap,in graphics).md) | Creates a CachedBitmap |
| [CachedBitmap::CachedBitmap(const CachedBitmap &)](..\gdiplusheaders\nf-gdiplusheaders-cachedbitmap-cachedbitmap(const cachedbitmap &).md) | Creates a CachedBitmap |
| [CachedBitmap::GetLastStatus](..\gdiplusheaders\nf-gdiplusheaders-cachedbitmap-getlaststatus.md) | The CachedBitmap |
| [CharacterRange::CharacterRange(INT,INT)](..\gdiplustypes\nf-gdiplustypes-characterrange-characterrange(int,int).md) | Creates a CharacterRange |
| [CharacterRange::CharacterRange~r2](..\gdiplustypes\nf-gdiplustypes-characterrange-characterrange~r2.md) | Creates a CharacterRange |
| [CharacterRange::operator=](..\gdiplustypes\nf-gdiplustypes-characterrange-operator=.md) | The CharacterRange |
| [Color::Color(IN ARGB)](..\gdipluscolor\nf-gdipluscolor-color-color(in argb).md) | Creates a Color |
| [Color::Color(IN BYTE,IN BYTE,IN BYTE)](..\gdipluscolor\nf-gdipluscolor-color-color(in byte,in byte,in byte).md) | Creates a Color |
| [Color::Color(IN BYTE,IN BYTE,IN BYTE,IN BYTE)](..\gdipluscolor\nf-gdipluscolor-color-color(in byte,in byte,in byte,in byte).md) | Creates a Color |
| [Color::Color](..\gdipluscolor\nf-gdipluscolor-color-color.md) | Creates a Color |
| [Color::GetA](..\gdipluscolor\nf-gdipluscolor-color-geta.md) | The Color |
| [Color::GetAlpha](..\gdipluscolor\nf-gdipluscolor-color-getalpha.md) | The Color |
| [Color::GetB](..\gdipluscolor\nf-gdipluscolor-color-getb.md) | The Color |
| [Color::GetBlue](..\gdipluscolor\nf-gdipluscolor-color-getblue.md) | The Color |
| [Color::GetG](..\gdipluscolor\nf-gdipluscolor-color-getg.md) | The Color |
| [Color::GetGreen](..\gdipluscolor\nf-gdipluscolor-color-getgreen.md) | The Color |
| [Color::GetR](..\gdipluscolor\nf-gdipluscolor-color-getr.md) | The Color |
| [Color::GetRed](..\gdipluscolor\nf-gdipluscolor-color-getred.md) | The Color |
| [Color::GetValue](..\gdipluscolor\nf-gdipluscolor-color-getvalue.md) | The Color |
| [Color::MakeARGB](..\gdipluscolor\nf-gdipluscolor-color-makeargb.md) | The Color |
| [Color::SetFromCOLORREF](..\gdipluscolor\nf-gdipluscolor-color-setfromcolorref.md) | The Color |
| [Color::SetValue](..\gdipluscolor\nf-gdipluscolor-color-setvalue.md) | The Color |
| [Color::ToCOLORREF](..\gdipluscolor\nf-gdipluscolor-color-tocolorref.md) | The Color |
| [ColorBalance::ColorBalance](..\gdipluseffects\nf-gdipluseffects-colorbalance-colorbalance.md) | Creates a new ColorBalance object. |
| [ColorBalance::GetParameters](..\gdipluseffects\nf-gdipluseffects-colorbalance-getparameters.md) | The ColorBalance |
| [ColorBalance::SetParameters](..\gdipluseffects\nf-gdipluseffects-colorbalance-setparameters.md) | The ColorBalance |
| [ColorCurve::ColorCurve](..\gdipluseffects\nf-gdipluseffects-colorcurve-colorcurve.md) | Creates a ColorCurve object. |
| [ColorCurve::GetParameters](..\gdipluseffects\nf-gdipluseffects-colorcurve-getparameters.md) | The ColorCurve |
| [ColorCurve::SetParameters](..\gdipluseffects\nf-gdipluseffects-colorcurve-setparameters.md) | The ColorCurve |
| [ColorLUT::ColorLUT](..\gdipluseffects\nf-gdipluseffects-colorlut-colorlut.md) | Creates a new ColorLUT object. |
| [ColorLUT::GetParameters](..\gdipluseffects\nf-gdipluseffects-colorlut-getparameters.md) | The ColorLUT |
| [ColorLUT::SetParameters](..\gdipluseffects\nf-gdipluseffects-colorlut-setparameters.md) | The ColorLUT |
| [ColorMatrixEffect::ColorMatrixEffect](..\gdipluseffects\nf-gdipluseffects-colormatrixeffect-colormatrixeffect.md) | Creates a ColorMatrixEffect object. |
| [ColorMatrixEffect::GetParameters](..\gdipluseffects\nf-gdipluseffects-colormatrixeffect-getparameters.md) | The ColorMatrixEffect |
| [ColorMatrixEffect::SetParameters](..\gdipluseffects\nf-gdipluseffects-colormatrixeffect-setparameters.md) | The ColorMatrixEffect |
| [CustomLineCap::Clone](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-clone.md) | The CustomLineCap |
| [CustomLineCap::CustomLineCap(GpCustomLineCap,Status)](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-customlinecap(gpcustomlinecap,status).md) | Creates a CustomLineCap |
| [CustomLineCap::CustomLineCap(IN const GraphicsPath,IN const GraphicsPath,IN LineCap,IN REAL)](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-customlinecap(in const graphicspath,in const graphicspath,in linecap,in real).md) | Creates a CustomLineCap |
| [CustomLineCap::CustomLineCap(const CustomLineCap &)](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-customlinecap(const customlinecap &).md) | Creates a CustomLineCap |
| [CustomLineCap::CustomLineCap~r2](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-customlinecap~r2.md) | Creates a CustomLineCap |
| [CustomLineCap::GetBaseCap](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-getbasecap.md) | The CustomLineCap |
| [CustomLineCap::GetBaseInset](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-getbaseinset.md) | The CustomLineCap |
| [CustomLineCap::GetLastStatus](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-getlaststatus.md) | The CustomLineCap |
| [CustomLineCap::GetStrokeCaps](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-getstrokecaps.md) | The CustomLineCap |
| [CustomLineCap::GetStrokeJoin](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-getstrokejoin.md) | The CustomLineCap |
| [CustomLineCap::GetWidthScale](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-getwidthscale.md) | The CustomLineCap |
| [CustomLineCap::SetBaseCap](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-setbasecap.md) | The CustomLineCap |
| [CustomLineCap::SetBaseInset](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-setbaseinset.md) | The CustomLineCap |
| [CustomLineCap::SetStrokeCap](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-setstrokecap.md) | The CustomLineCap |
| [CustomLineCap::SetStrokeCaps](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-setstrokecaps.md) | The CustomLineCap |
| [CustomLineCap::SetStrokeJoin](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-setstrokejoin.md) | The CustomLineCap |
| [CustomLineCap::SetWidthScale](..\gdiplusheaders\nf-gdiplusheaders-customlinecap-setwidthscale.md) | The CustomLineCap |
| [Effect::Effect](..\gdipluseffects\nf-gdipluseffects-effect-effect.md) | Creates an Effect object. |
| [Effect::GetAuxDataSize](..\gdipluseffects\nf-gdipluseffects-effect-getauxdatasize.md) | The Effect |
| [Effect::GetAuxData](..\gdipluseffects\nf-gdipluseffects-effect-getauxdata.md) | The Effect |
| [Effect::GetParameterSize](..\gdipluseffects\nf-gdipluseffects-effect-getparametersize.md) | The Effect |
| [Effect::UseAuxData](..\gdipluseffects\nf-gdipluseffects-effect-useauxdata.md) | The Effect |
| [Font::Clone](..\gdiplusheaders\nf-gdiplusheaders-font-clone.md) | The Font |
| [Font::GetFamily](..\gdiplusheaders\nf-gdiplusheaders-font-getfamily.md) | The Font |
| [Font::GetLastStatus](..\gdiplusheaders\nf-gdiplusheaders-font-getlaststatus.md) | The Font |
| [Font::GetLogFontA](..\gdiplusheaders\nf-gdiplusheaders-font-getlogfonta.md) | The Font |
| [Font::GetLogFontW](..\gdiplusheaders\nf-gdiplusheaders-font-getlogfontw.md) | The Font |
| [Font::GetSize](..\gdiplusheaders\nf-gdiplusheaders-font-getsize.md) | The Font |
| [Font::GetStyle](..\gdiplusheaders\nf-gdiplusheaders-font-getstyle.md) | The Font |
| [Font::GetUnit](..\gdiplusheaders\nf-gdiplusheaders-font-getunit.md) | The Font |
| [Font::IsAvailable](..\gdiplusheaders\nf-gdiplusheaders-font-isavailable.md) | The Font |
| [FontCollection::FontCollection(const FontCollection &)](..\gdiplusheaders\nf-gdiplusheaders-fontcollection-fontcollection(const fontcollection &).md) | Creates an empty FontCollection |
| [FontCollection::FontCollection](..\gdiplusheaders\nf-gdiplusheaders-fontcollection-fontcollection.md) | Creates an empty FontCollection |
| [FontCollection::GetFamilies](..\gdiplusheaders\nf-gdiplusheaders-fontcollection-getfamilies.md) | The FontCollection |
| [FontCollection::GetFamilyCount](..\gdiplusheaders\nf-gdiplusheaders-fontcollection-getfamilycount.md) | The FontCollection |
| [FontCollection::GetLastStatus](..\gdiplusheaders\nf-gdiplusheaders-fontcollection-getlaststatus.md) | The FontCollection |
| [FontFamily::Clone](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-clone.md) | The FontFamily |
| [FontFamily::FontFamily(GpFontFamily,Status)](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-fontfamily(gpfontfamily,status).md) | Creates an empty FontFamily |
| [FontFamily::FontFamily(IN const WCHAR,IN const FontCollection)](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-fontfamily(in const wchar,in const fontcollection).md) | Creates an empty FontFamily |
| [FontFamily::FontFamily(const FontFamily &)](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-fontfamily(const fontfamily &).md) | Creates an empty FontFamily |
| [FontFamily::FontFamily](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-fontfamily.md) | Creates an empty FontFamily |
| [FontFamily::GenericMonospace](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-genericmonospace.md) | The FontFamily |
| [FontFamily::GenericSansSerif](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-genericsansserif.md) | The FontFamily |
| [FontFamily::GenericSerif](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-genericserif.md) | The FontFamily |
| [FontFamily::GetCellAscent](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-getcellascent.md) | The FontFamily |
| [FontFamily::GetCellDescent](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-getcelldescent.md) | The FontFamily |
| [FontFamily::GetEmHeight](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-getemheight.md) | The FontFamily |
| [FontFamily::GetFamilyName](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-getfamilyname.md) | The FontFamily |
| [FontFamily::GetLastStatus](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-getlaststatus.md) | The FontFamily |
| [FontFamily::GetLineSpacing](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-getlinespacing.md) | The FontFamily |
| [FontFamily::IsAvailable](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-isavailable.md) | The FontFamily |
| [FontFamily::IsStyleAvailable](..\gdiplusheaders\nf-gdiplusheaders-fontfamily-isstyleavailable.md) | The FontFamily |
| [GdiplusBase::operator delete[]](..\gdiplusbase\nf-gdiplusbase-gdiplusbase-operator delete[].md) | The xref rid=&#0034;_gdiplus_CLASS_GdiplusBase_operator_delete_bracket_in_pVoid_&#0034; qualify=&#0034;0&#0034;/&gt; method deallocates memory for an array of Windows GDI+ objects. |
| [GdiplusBase::operator delete](..\gdiplusbase\nf-gdiplusbase-gdiplusbase-operator delete.md) | The GdiplusBase |
| [GdiplusBase::operator new[]](..\gdiplusbase\nf-gdiplusbase-gdiplusbase-operator new[].md) | The GdiplusBase |
| [GdiplusBase::operator new](..\gdiplusbase\nf-gdiplusbase-gdiplusbase-operator new.md) | The GdiplusBase |
| [Graphics::AddMetafileComment](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-addmetafilecomment.md) | The Graphics |
| [Graphics::BeginContainer(IN const Rect &,IN const Rect &,IN Unit)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-begincontainer(in const rect &,in const rect &,in unit).md) | The Graphics |
| [Graphics::BeginContainer](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-begincontainer.md) | The Graphics |
| [Graphics::Clear](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-clear.md) | The Graphics |
| [Graphics::DrawArc(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawarc(in const pen,in int,in int,in int,in int,in real,in real).md) | This topic lists the DrawArc methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawArc(IN const Pen,IN const Rect &,IN REAL,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawarc(in const pen,in const rect &,in real,in real).md) | This topic lists the DrawArc methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawArc(IN const Pen,IN const RectF &,IN REAL,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawarc(in const pen,in const rectf &,in real,in real).md) | This topic lists the DrawArc methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawArc](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawarc.md) | This topic lists the DrawArc methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawBezier(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawbezier(in const pen,in int,in int,in int,in int,in int,in int,in int,in int).md) | This topic lists the DrawBezier methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawBezier(IN const Pen,IN const Point &,IN const Point &,IN const Point &,IN const Point &)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawbezier(in const pen,in const point &,in const point &,in const point &,in const point &).md) | This topic lists the DrawBezier methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawBezier(IN const Pen,IN const PointF &,IN const PointF &,IN const PointF &,IN const PointF &)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawbezier(in const pen,in const pointf &,in const pointf &,in const pointf &,in const pointf &).md) | This topic lists the DrawBezier methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawBezier](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawbezier.md) | This topic lists the DrawBezier methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawBeziers(IN const Pen,IN const Point,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawbeziers(in const pen,in const point,in int).md) | This topic lists the DrawBeziers methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawBeziers](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawbeziers.md) | This topic lists the DrawBeziers methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawCachedBitmap](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawcachedbitmap.md) | The Graphics |
| [Graphics::DrawClosedCurve(IN const Pen,IN const Point,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawclosedcurve(in const pen,in const point,in int).md) | This topic lists the DrawClosedCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawClosedCurve(IN const Pen,IN const Point,IN INT,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawclosedcurve(in const pen,in const point,in int,in real).md) | This topic lists the DrawClosedCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawClosedCurve(IN const Pen,IN const PointF,IN INT,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawclosedcurve(in const pen,in const pointf,in int,in real).md) | This topic lists the DrawClosedCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawClosedCurve](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawclosedcurve.md) | This topic lists the DrawClosedCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawCurve(IN const Pen,IN const Point,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawcurve(in const pen,in const point,in int).md) | This topic lists the DrawCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawCurve(IN const Pen,IN const Point,IN INT,IN INT,IN INT,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawcurve(in const pen,in const point,in int,in int,in int,in real).md) | This topic lists the DrawCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawCurve(IN const Pen,IN const Point,IN INT,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawcurve(in const pen,in const point,in int,in real).md) | This topic lists the DrawCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawCurve(IN const Pen,IN const PointF,IN INT,IN INT,IN INT,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawcurve(in const pen,in const pointf,in int,in int,in int,in real).md) | This topic lists the DrawCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawCurve(IN const Pen,IN const PointF,IN INT,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawcurve(in const pen,in const pointf,in int,in real).md) | This topic lists the DrawCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawCurve](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawcurve.md) | This topic lists the DrawCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawDriverString](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawdriverstring.md) | The Graphics |
| [Graphics::DrawLines(IN const Pen,IN const Point,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawlines(in const pen,in const point,in int).md) | This topic lists the DrawLines methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawLines](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawlines.md) | This topic lists the DrawLines methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawPath](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawpath.md) | The Graphics |
| [Graphics::DrawPie(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawpie(in const pen,in int,in int,in int,in int,in real,in real).md) | This topic lists the DrawPie methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawPie(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawpie(in const pen,in real,in real,in real,in real,in real,in real).md) | This topic lists the DrawPie methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawPie(IN const Pen,IN const Rect &,IN REAL,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawpie(in const pen,in const rect &,in real,in real).md) | This topic lists the DrawPie methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawPie](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawpie.md) | This topic lists the DrawPie methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawPolygon(IN const Pen,IN const Point,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawpolygon(in const pen,in const point,in int).md) | This topic lists the DrawPolygon methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawPolygon](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawpolygon.md) | This topic lists the DrawPolygon methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawRectangles(IN const Pen,IN const Rect,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawrectangles(in const pen,in const rect,in int).md) | This topic lists the DrawRectangles methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawRectangles](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawrectangles.md) | This topic lists the DrawRectangles methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawString(const WCHAR,INT,const Font,const PointF &,const Brush)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawstring(const wchar,int,const font,const pointf &,const brush).md) | This topic lists the DrawString methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawString(const WCHAR,INT,const Font,const PointF &,const StringFormat,const Brush)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawstring(const wchar,int,const font,const pointf &,const stringformat,const brush).md) | This topic lists the DrawString methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::DrawString](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-drawstring.md) | This topic lists the DrawString methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EndContainer](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-endcontainer.md) | The Graphics |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const Point &,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const point &,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const Point &,IN const Rect &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const point &,in const rect &,in unit,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const Point,IN INT,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const point,in int,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const Point,IN INT,IN const Rect &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const point,in int,in const rect &,in unit,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const PointF &,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const pointf &,in const rectf &,in unit,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const PointF,IN INT,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const pointf,in int,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const PointF,IN INT,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const pointf,in int,in const rectf &,in unit,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const Rect &,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const rect &,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const Rect &,IN const Rect &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const rect &,in const rect &,in unit,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const RectF &,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const rectf &,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile(IN const Metafile,IN const RectF &,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile(in const metafile,in const rectf &,in const rectf &,in unit,in enumeratemetafileproc,in void,in const imageattributes).md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::EnumerateMetafile](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-enumeratemetafile.md) | This topic lists the EnumerateMetafile methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::ExcludeClip(IN const Rect &)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-excludeclip(in const rect &).md) | This topic lists the ExcludeClip methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::ExcludeClip(IN const Region)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-excludeclip(in const region).md) | This topic lists the ExcludeClip methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::ExcludeClip](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-excludeclip.md) | This topic lists the ExcludeClip methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillclosedcurve(in const brush,in const point,in int).md) | This topic lists the FillClosedCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT,IN FillMode,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillclosedcurve(in const brush,in const point,in int,in fillmode,in real).md) | This topic lists the FillClosedCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillClosedCurve(IN const Brush,IN const PointF,IN INT,IN FillMode,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillclosedcurve(in const brush,in const pointf,in int,in fillmode,in real).md) | This topic lists the FillClosedCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillClosedCurve](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillclosedcurve.md) | This topic lists the FillClosedCurve methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillPath](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillpath.md) | The Graphics |
| [Graphics::FillPie(IN const Brush,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillpie(in const brush,in int,in int,in int,in int,in real,in real).md) | This topic lists the FillPie methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillPie(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillpie(in const brush,in real,in real,in real,in real,in real,in real).md) | This topic lists the FillPie methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillPie(IN const Brush,IN const Rect &,IN REAL,IN REAL)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillpie(in const brush,in const rect &,in real,in real).md) | This topic lists the FillPie methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillPie](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillpie.md) | This topic lists the FillPie methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillPolygon(IN const Brush,IN const Point,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillpolygon(in const brush,in const point,in int).md) | This topic lists the FillPolygon methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillPolygon(IN const Brush,IN const Point,IN INT,IN FillMode)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillpolygon(in const brush,in const point,in int,in fillmode).md) | This topic lists the FillPolygon methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillPolygon(IN const Brush,IN const PointF,IN INT,IN FillMode)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillpolygon(in const brush,in const pointf,in int,in fillmode).md) | This topic lists the FillPolygon methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillPolygon](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillpolygon.md) | This topic lists the FillPolygon methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillRectangles(IN const Brush,IN const Rect,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillrectangles(in const brush,in const rect,in int).md) | This topic lists the FillRectangles methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillRectangles](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillrectangles.md) | This topic lists the FillRectangles methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FillRegion](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fillregion.md) | The Graphics |
| [Graphics::Flush](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-flush.md) | The Graphics |
| [Graphics::FromHDC(IN HDC)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fromhdc(in hdc).md) | This topic lists the FromHDC methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FromHDC(IN HDC,IN HANDLE)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fromhdc(in hdc,in handle).md) | This topic lists the FromHDC methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::FromHWND](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fromhwnd.md) | The Graphics |
| [Graphics::FromImage](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-fromimage.md) | The Graphics |
| [Graphics::GetClipBounds(OUT Rect)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getclipbounds(out rect).md) | This topic lists the GetClipBounds methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::GetClipBounds](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getclipbounds.md) | This topic lists the GetClipBounds methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::GetClip](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getclip.md) | The Graphics |
| [Graphics::GetCompositingMode](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getcompositingmode.md) | The Graphics |
| [Graphics::GetCompositingQuality](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getcompositingquality.md) | The Graphics |
| [Graphics::GetDpiX](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getdpix.md) | The Graphics |
| [Graphics::GetDpiY](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getdpiy.md) | The Graphics |
| [Graphics::GetHDC](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-gethdc.md) | The Graphics |
| [Graphics::GetHalftonePalette](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-gethalftonepalette.md) | The Graphics |
| [Graphics::GetInterpolationMode](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getinterpolationmode.md) | The Graphics |
| [Graphics::GetLastStatus](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getlaststatus.md) | The Graphics |
| [Graphics::GetNearestColor](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getnearestcolor.md) | The Graphics |
| [Graphics::GetPageScale](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getpagescale.md) | The Graphics |
| [Graphics::GetPageUnit](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getpageunit.md) | The Graphics |
| [Graphics::GetPixelOffsetMode](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getpixeloffsetmode.md) | The Graphics |
| [Graphics::GetRenderingOrigin](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getrenderingorigin.md) | The Graphics |
| [Graphics::GetSmoothingMode](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getsmoothingmode.md) | The Graphics |
| [Graphics::GetTextContrast](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-gettextcontrast.md) | The Graphics |
| [Graphics::GetTextRenderingHint](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-gettextrenderinghint.md) | The Graphics |
| [Graphics::GetTransform](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-gettransform.md) | The Graphics |
| [Graphics::GetVisibleClipBounds(OUT Rect)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getvisibleclipbounds(out rect).md) | This topic lists the GetVisibleClipBounds methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::GetVisibleClipBounds](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-getvisibleclipbounds.md) | This topic lists the GetVisibleClipBounds methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::IntersectClip(IN const Rect &)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-intersectclip(in const rect &).md) | This topic lists the InterscetClip methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::IntersectClip(IN const Region)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-intersectclip(in const region).md) | This topic lists the InterscetClip methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::IntersectClip](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-intersectclip.md) | This topic lists the InterscetClip methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::IsClipEmpty](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-isclipempty.md) | The Graphics |
| [Graphics::IsVisibleClipEmpty](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-isvisibleclipempty.md) | The Graphics |
| [Graphics::MeasureCharacterRanges](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-measurecharacterranges.md) | The Graphics |
| [Graphics::MeasureDriverString](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-measuredriverstring.md) | The Graphics |
| [Graphics::MultiplyTransform](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-multiplytransform.md) | The Graphics |
| [Graphics::ReleaseHDC](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-releasehdc.md) | The Graphics |
| [Graphics::ResetClip](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-resetclip.md) | The Graphics |
| [Graphics::ResetTransform](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-resettransform.md) | The Graphics |
| [Graphics::Restore](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-restore.md) | The Graphics |
| [Graphics::RotateTransform](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-rotatetransform.md) | The Graphics |
| [Graphics::Save](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-save.md) | The Graphics |
| [Graphics::ScaleTransform](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-scaletransform.md) | The Graphics |
| [Graphics::SetAbort](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-setabort.md) | Not used in Windows GDI+ versions 1.0 and 1.1. |
| [Graphics::SetCompositingMode](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-setcompositingmode.md) | The Graphics |
| [Graphics::SetCompositingQuality](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-setcompositingquality.md) | The Graphics |
| [Graphics::SetInterpolationMode](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-setinterpolationmode.md) | The Graphics |
| [Graphics::SetPageScale](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-setpagescale.md) | The Graphics |
| [Graphics::SetPageUnit](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-setpageunit.md) | The Graphics |
| [Graphics::SetPixelOffsetMode](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-setpixeloffsetmode.md) | The Graphics |
| [Graphics::SetRenderingOrigin](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-setrenderingorigin.md) | The Graphics |
| [Graphics::SetSmoothingMode](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-setsmoothingmode.md) | The Graphics |
| [Graphics::SetTextContrast](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-settextcontrast.md) | The Graphics |
| [Graphics::SetTextRenderingHint](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-settextrenderinghint.md) | The Graphics |
| [Graphics::SetTransform](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-settransform.md) | The Graphics |
| [Graphics::TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-transformpoints(in coordinatespace,in coordinatespace,in out point,in int).md) | The Graphics |
| [Graphics::TransformPoints](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-transformpoints.md) | The Graphics |
| [Graphics::TranslateClip(IN INT,IN INT)](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-translateclip(in int,in int).md) | This topic lists the TranslateClip methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::TranslateClip](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-translateclip.md) | This topic lists the TranslateClip methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics. |
| [Graphics::TranslateTransform](..\gdiplusgraphics\nf-gdiplusgraphics-graphics-translatetransform.md) | The Graphics |
| [GraphicsPath::AddClosedCurve(IN const Point,IN INT)](..\gdipluspath\nf-gdipluspath-graphicspath-addclosedcurve(in const point,in int).md) | This topic lists the AddClosedCurve methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddClosedCurve(IN const Point,IN INT,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addclosedcurve(in const point,in int,in real).md) | This topic lists the AddClosedCurve methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddClosedCurve(IN const PointF,IN INT,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addclosedcurve(in const pointf,in int,in real).md) | This topic lists the AddClosedCurve methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddClosedCurve](..\gdipluspath\nf-gdipluspath-graphicspath-addclosedcurve.md) | This topic lists the AddClosedCurve methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddCurve(IN const Point,IN INT)](..\gdipluspath\nf-gdipluspath-graphicspath-addcurve(in const point,in int).md) | This topic lists the AddCurve methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddCurve(IN const Point,IN INT,IN INT,IN INT,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addcurve(in const point,in int,in int,in int,in real).md) | This topic lists the AddCurve methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddCurve(IN const Point,IN INT,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addcurve(in const point,in int,in real).md) | This topic lists the AddCurve methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddCurve(IN const PointF,IN INT,IN INT,IN INT,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addcurve(in const pointf,in int,in int,in int,in real).md) | This topic lists the AddCurve methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddCurve(IN const PointF,IN INT,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addcurve(in const pointf,in int,in real).md) | This topic lists the AddCurve methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddCurve](..\gdipluspath\nf-gdipluspath-graphicspath-addcurve.md) | This topic lists the AddCurve methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddEllipse(IN INT,IN INT,IN INT,IN INT)](..\gdipluspath\nf-gdipluspath-graphicspath-addellipse(in int,in int,in int,in int).md) | This topic lists the AddEllipse methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddEllipse(IN REAL,IN REAL,IN REAL,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addellipse(in real,in real,in real,in real).md) | This topic lists the AddEllipse methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddEllipse(IN const Rect &)](..\gdipluspath\nf-gdipluspath-graphicspath-addellipse(in const rect &).md) | This topic lists the AddEllipse methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddEllipse](..\gdipluspath\nf-gdipluspath-graphicspath-addellipse.md) | This topic lists the AddEllipse methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddLine(IN INT,IN INT,IN INT,IN INT)](..\gdipluspath\nf-gdipluspath-graphicspath-addline(in int,in int,in int,in int).md) | This topic lists the AddLine methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddLine(IN REAL,IN REAL,IN REAL,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addline(in real,in real,in real,in real).md) | This topic lists the AddLine methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddLine(IN const Point &,IN const Point &)](..\gdipluspath\nf-gdipluspath-graphicspath-addline(in const point &,in const point &).md) | This topic lists the AddLine methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddLine](..\gdipluspath\nf-gdipluspath-graphicspath-addline.md) | This topic lists the AddLine methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddPath](..\gdipluspath\nf-gdipluspath-graphicspath-addpath.md) | The GraphicsPath |
| [GraphicsPath::AddPie(IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addpie(in int,in int,in int,in int,in real,in real).md) | This topic lists the AddPie methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddPie(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addpie(in real,in real,in real,in real,in real,in real).md) | This topic lists the AddPie methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddPie(IN const Rect &,IN REAL,IN REAL)](..\gdipluspath\nf-gdipluspath-graphicspath-addpie(in const rect &,in real,in real).md) | This topic lists the AddPie methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddPie](..\gdipluspath\nf-gdipluspath-graphicspath-addpie.md) | This topic lists the AddPie methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddPolygon(IN const Point,IN INT)](..\gdipluspath\nf-gdipluspath-graphicspath-addpolygon(in const point,in int).md) | This topic lists the AddPolygon methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddPolygon](..\gdipluspath\nf-gdipluspath-graphicspath-addpolygon.md) | This topic lists the AddPolygon methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddRectangle(IN const Rect &)](..\gdipluspath\nf-gdipluspath-graphicspath-addrectangle(in const rect &).md) | This topic lists the AddRectangle methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddRectangle](..\gdipluspath\nf-gdipluspath-graphicspath-addrectangle.md) | This topic lists the AddRectangle methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddRectangles(IN const Rect,INT)](..\gdipluspath\nf-gdipluspath-graphicspath-addrectangles(in const rect,int).md) | This topic lists the AddRectangles methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::AddRectangles](..\gdipluspath\nf-gdipluspath-graphicspath-addrectangles.md) | This topic lists the AddRectangles methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::ClearMarkers](..\gdipluspath\nf-gdipluspath-graphicspath-clearmarkers.md) | The GraphicsPath |
| [GraphicsPath::Clone](..\gdipluspath\nf-gdipluspath-graphicspath-clone.md) | The GraphicsPath |
| [GraphicsPath::CloseAllFigures](..\gdipluspath\nf-gdipluspath-graphicspath-closeallfigures.md) | The GraphicsPath |
| [GraphicsPath::CloseFigure](..\gdipluspath\nf-gdipluspath-graphicspath-closefigure.md) | The GraphicsPath |
| [GraphicsPath::Flatten](..\gdipluspath\nf-gdipluspath-graphicspath-flatten.md) | The GraphicsPath |
| [GraphicsPath::GetFillMode](..\gdipluspath\nf-gdipluspath-graphicspath-getfillmode.md) | The GraphicsPath |
| [GraphicsPath::GetLastPoint](..\gdipluspath\nf-gdipluspath-graphicspath-getlastpoint.md) | The GraphicsPath |
| [GraphicsPath::GetLastStatus](..\gdipluspath\nf-gdipluspath-graphicspath-getlaststatus.md) | The GraphicsPath |
| [GraphicsPath::GetPathData](..\gdipluspath\nf-gdipluspath-graphicspath-getpathdata.md) | The GraphicsPath |
| [GraphicsPath::GetPathPoints(OUT Point,IN INT)](..\gdipluspath\nf-gdipluspath-graphicspath-getpathpoints(out point,in int).md) | This topic lists the GetPathPoints methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::GetPathPoints](..\gdipluspath\nf-gdipluspath-graphicspath-getpathpoints.md) | This topic lists the GetPathPoints methods of the GraphicsPath class. For a complete list of methods for the GraphicsPath class, see GraphicsPath. |
| [GraphicsPath::GetPathTypes](..\gdipluspath\nf-gdipluspath-graphicspath-getpathtypes.md) | The GraphicsPath |
| [GraphicsPath::GetPointCount](..\gdipluspath\nf-gdipluspath-graphicspath-getpointcount.md) | The GraphicsPath |
| [GraphicsPath::Outline](..\gdipluspath\nf-gdipluspath-graphicspath-outline.md) | The GraphicsPath |
| [GraphicsPath::Reset](..\gdipluspath\nf-gdipluspath-graphicspath-reset.md) | The GraphicsPath |
| [GraphicsPath::Reverse](..\gdipluspath\nf-gdipluspath-graphicspath-reverse.md) | The GraphicsPath |
| [GraphicsPath::SetFillMode](..\gdipluspath\nf-gdipluspath-graphicspath-setfillmode.md) | The GraphicsPath |
| [GraphicsPath::SetMarker](..\gdipluspath\nf-gdipluspath-graphicspath-setmarker.md) | The GraphicsPath |
| [GraphicsPath::StartFigure](..\gdipluspath\nf-gdipluspath-graphicspath-startfigure.md) | The GraphicsPath |
| [GraphicsPath::Transform](..\gdipluspath\nf-gdipluspath-graphicspath-transform.md) | The GraphicsPath |
| [GraphicsPath::Warp](..\gdipluspath\nf-gdipluspath-graphicspath-warp.md) | The GraphicsPath |
| [GraphicsPath::Widen](..\gdipluspath\nf-gdipluspath-graphicspath-widen.md) | The GraphicsPath |
| [GraphicsPathIterator::CopyData](..\gdipluspath\nf-gdipluspath-graphicspathiterator-copydata.md) | The GraphicsPathIterator |
| [GraphicsPathIterator::Enumerate](..\gdipluspath\nf-gdipluspath-graphicspathiterator-enumerate.md) | The GraphicsPathIterator |
| [GraphicsPathIterator::GetCount](..\gdipluspath\nf-gdipluspath-graphicspathiterator-getcount.md) | The GraphicsPathIterator |
| [GraphicsPathIterator::GetLastStatus](..\gdipluspath\nf-gdipluspath-graphicspathiterator-getlaststatus.md) | The GraphicsPathIterator |
| [GraphicsPathIterator::GetSubpathCount](..\gdipluspath\nf-gdipluspath-graphicspathiterator-getsubpathcount.md) | The GraphicsPathIterator |
| [GraphicsPathIterator::GraphicsPathIterator(IN const GraphicsPath)](..\gdipluspath\nf-gdipluspath-graphicspathiterator-graphicspathiterator(in const graphicspath).md) | Creates a new GraphicsPathIterator |
| [GraphicsPathIterator::GraphicsPathIterator(const GraphicsPathIterator &)](..\gdipluspath\nf-gdipluspath-graphicspathiterator-graphicspathiterator(const graphicspathiterator &).md) | Creates a new GraphicsPathIterator |
| [GraphicsPathIterator::HasCurve](..\gdipluspath\nf-gdipluspath-graphicspathiterator-hascurve.md) | The GraphicsPathIterator |
| [GraphicsPathIterator::NextMarker(OUT const GraphicsPath)](..\gdipluspath\nf-gdipluspath-graphicspathiterator-nextmarker(out const graphicspath).md) | This topic lists the NextMarker methods of the GraphicsPathIterator class. For a complete list of methods for the GraphicsPathIterator class, see GraphicsPathIterator Methods. |
| [GraphicsPathIterator::NextMarker](..\gdipluspath\nf-gdipluspath-graphicspathiterator-nextmarker.md) | This topic lists the NextMarker methods of the GraphicsPathIterator class. For a complete list of methods for the GraphicsPathIterator class, see GraphicsPathIterator Methods. |
| [GraphicsPathIterator::NextPathType](..\gdipluspath\nf-gdipluspath-graphicspathiterator-nextpathtype.md) | The GraphicsPathIterator |
| [GraphicsPathIterator::NextSubpath(OUT const GraphicsPath,OUT BOOL)](..\gdipluspath\nf-gdipluspath-graphicspathiterator-nextsubpath(out const graphicspath,out bool).md) | This topic lists the NextSubpath methods of the GraphicsPathIterator class. For a complete list of methods for the GraphicsPathIterator class, see GraphicsPathIterator Methods. |
| [GraphicsPathIterator::NextSubpath](..\gdipluspath\nf-gdipluspath-graphicspathiterator-nextsubpath.md) | This topic lists the NextSubpath methods of the GraphicsPathIterator class. For a complete list of methods for the GraphicsPathIterator class, see GraphicsPathIterator Methods. |
| [GraphicsPathIterator::Rewind](..\gdipluspath\nf-gdipluspath-graphicspathiterator-rewind.md) | The GraphicsPathIterator |
| [HatchBrush::GetBackgroundColor](..\gdiplusbrush\nf-gdiplusbrush-hatchbrush-getbackgroundcolor.md) | The HatchBrush |
| [HatchBrush::GetForegroundColor](..\gdiplusbrush\nf-gdiplusbrush-hatchbrush-getforegroundcolor.md) | The HatchBrush |
| [HatchBrush::GetHatchStyle](..\gdiplusbrush\nf-gdiplusbrush-hatchbrush-gethatchstyle.md) | The HatchBrush |
| [HatchBrush::HatchBrush(IN HatchStyle,IN const Color &,IN const Color &)](..\gdiplusbrush\nf-gdiplusbrush-hatchbrush-hatchbrush(in hatchstyle,in const color &,in const color &).md) | Creates a HatchBrush |
| [HatchBrush::HatchBrush(const HatchBrush &)](..\gdiplusbrush\nf-gdiplusbrush-hatchbrush-hatchbrush(const hatchbrush &).md) | Creates a HatchBrush |
| [HatchBrush::HatchBrush~r3](..\gdiplusbrush\nf-gdiplusbrush-hatchbrush-hatchbrush~r3.md) | Creates a HatchBrush |
| [HueSaturationLightness::GetParameters](..\gdipluseffects\nf-gdipluseffects-huesaturationlightness-getparameters.md) | The HueSaturationLightness |
| [HueSaturationLightness::HueSaturationLightness](..\gdipluseffects\nf-gdipluseffects-huesaturationlightness-huesaturationlightness.md) | Creates a HueSaturationLightness object. |
| [HueSaturationLightness::SetParameters](..\gdipluseffects\nf-gdipluseffects-huesaturationlightness-setparameters.md) | The HueSaturationLightness |
| [Image::Clone](..\gdiplusheaders\nf-gdiplusheaders-image-clone.md) | The Image |
| [Image::FindFirstItem](..\gdiplusheaders\nf-gdiplusheaders-image-findfirstitem.md) | The Image |
| [Image::FindNextItem](..\gdiplusheaders\nf-gdiplusheaders-image-findnextitem.md) | The Image |
| [Image::FromFile](..\gdiplusheaders\nf-gdiplusheaders-image-fromfile.md) | The Image |
| [Image::FromStream](..\gdiplusheaders\nf-gdiplusheaders-image-fromstream.md) | The Image |
| [Image::GetAllPropertyItems](..\gdiplusheaders\nf-gdiplusheaders-image-getallpropertyitems.md) | The Image |
| [Image::GetBounds](..\gdiplusheaders\nf-gdiplusheaders-image-getbounds.md) | The Image |
| [Image::GetEncoderParameterListSize](..\gdiplusheaders\nf-gdiplusheaders-image-getencoderparameterlistsize.md) | The Image |
| [Image::GetEncoderParameterList](..\gdiplusheaders\nf-gdiplusheaders-image-getencoderparameterlist.md) | The Image |
| [Image::GetFlags](..\gdiplusheaders\nf-gdiplusheaders-image-getflags.md) | The Image |
| [Image::GetFrameCount](..\gdiplusheaders\nf-gdiplusheaders-image-getframecount.md) | The Image |
| [Image::GetFrameDimensionsCount](..\gdiplusheaders\nf-gdiplusheaders-image-getframedimensionscount.md) | The Image |
| [Image::GetFrameDimensionsList](..\gdiplusheaders\nf-gdiplusheaders-image-getframedimensionslist.md) | The Image |
| [Image::GetHeight](..\gdiplusheaders\nf-gdiplusheaders-image-getheight.md) | The Image |
| [Image::GetHorizontalResolution](..\gdiplusheaders\nf-gdiplusheaders-image-gethorizontalresolution.md) | The Image |
| [Image::GetItemData](..\gdiplusheaders\nf-gdiplusheaders-image-getitemdata.md) | The Image |
| [Image::GetLastStatus](..\gdiplusheaders\nf-gdiplusheaders-image-getlaststatus.md) | The Image |
| [Image::GetPaletteSize](..\gdiplusheaders\nf-gdiplusheaders-image-getpalettesize.md) | The Image |
| [Image::GetPalette](..\gdiplusheaders\nf-gdiplusheaders-image-getpalette.md) | The Image |
| [Image::GetPhysicalDimension](..\gdiplusheaders\nf-gdiplusheaders-image-getphysicaldimension.md) | The Image |
| [Image::GetPixelFormat](..\gdiplusheaders\nf-gdiplusheaders-image-getpixelformat.md) | The Image |
| [Image::GetPropertyCount](..\gdiplusheaders\nf-gdiplusheaders-image-getpropertycount.md) | The Image |
| [Image::GetPropertyIdList](..\gdiplusheaders\nf-gdiplusheaders-image-getpropertyidlist.md) | The Image |
| [Image::GetPropertyItemSize](..\gdiplusheaders\nf-gdiplusheaders-image-getpropertyitemsize.md) | The Image |
| [Image::GetPropertyItem](..\gdiplusheaders\nf-gdiplusheaders-image-getpropertyitem.md) | The Image |
| [Image::GetPropertySize](..\gdiplusheaders\nf-gdiplusheaders-image-getpropertysize.md) | The Image |
| [Image::GetRawFormat](..\gdiplusheaders\nf-gdiplusheaders-image-getrawformat.md) | The Image |
| [Image::GetThumbnailImage](..\gdiplusheaders\nf-gdiplusheaders-image-getthumbnailimage.md) | The Image |
| [Image::GetType](..\gdiplusheaders\nf-gdiplusheaders-image-gettype.md) | The Image |
| [Image::GetVerticalResolution](..\gdiplusheaders\nf-gdiplusheaders-image-getverticalresolution.md) | The Image |
| [Image::GetWidth](..\gdiplusheaders\nf-gdiplusheaders-image-getwidth.md) | The Image |
| [Image::RemovePropertyItem](..\gdiplusheaders\nf-gdiplusheaders-image-removepropertyitem.md) | The Image |
| [Image::RotateFlip](..\gdiplusheaders\nf-gdiplusheaders-image-rotateflip.md) | The Image |
| [Image::SaveAdd(IN Image,IN const EncoderParameters)](..\gdiplusheaders\nf-gdiplusheaders-image-saveadd(in image,in const encoderparameters).md) | This topic lists the SaveAdd methods of the Image class. For a complete list of methods for the Image class, see Image Methods. |
| [Image::SaveAdd](..\gdiplusheaders\nf-gdiplusheaders-image-saveadd.md) | This topic lists the SaveAdd methods of the Image class. For a complete list of methods for the Image class, see Image Methods. |
| [Image::SelectActiveFrame](..\gdiplusheaders\nf-gdiplusheaders-image-selectactiveframe.md) | The Image |
| [Image::SetAbort](..\gdiplusheaders\nf-gdiplusheaders-image-setabort.md) | The Image |
| [Image::SetPalette](..\gdiplusheaders\nf-gdiplusheaders-image-setpalette.md) | The Image |
| [Image::SetPropertyItem](..\gdiplusheaders\nf-gdiplusheaders-image-setpropertyitem.md) | The Image |
| [ImageAttributes::ClearBrushRemapTable](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-clearbrushremaptable.md) | The ImageAttributes |
| [ImageAttributes::ClearColorKey](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-clearcolorkey.md) | The ImageAttributes |
| [ImageAttributes::ClearColorMatrices](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-clearcolormatrices.md) | The ImageAttributes |
| [ImageAttributes::ClearColorMatrix](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-clearcolormatrix.md) | The ImageAttributes |
| [ImageAttributes::ClearGamma](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-cleargamma.md) | The ImageAttributes |
| [ImageAttributes::ClearNoOp](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-clearnoop.md) | The ImageAttributes |
| [ImageAttributes::ClearOutputChannelColorProfile](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-clearoutputchannelcolorprofile.md) | The ImageAttributes |
| [ImageAttributes::ClearOutputChannel](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-clearoutputchannel.md) | The ImageAttributes |
| [ImageAttributes::ClearRemapTable](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-clearremaptable.md) | The ImageAttributes |
| [ImageAttributes::ClearThreshold](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-clearthreshold.md) | The ImageAttributes |
| [ImageAttributes::Clone](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-clone.md) | The ImageAttributes |
| [ImageAttributes::GetAdjustedPalette](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-getadjustedpalette.md) | The ImageAttributes |
| [ImageAttributes::GetLastStatus](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-getlaststatus.md) | The ImageAttributes |
| [ImageAttributes::ImageAttributes(GpImageAttributes,Status)](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-imageattributes(gpimageattributes,status).md) | Creates an ImageAttributes |
| [ImageAttributes::ImageAttributes(const ImageAttributes &)](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-imageattributes(const imageattributes &).md) | Creates an ImageAttributes |
| [ImageAttributes::ImageAttributes](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-imageattributes.md) | Creates an ImageAttributes |
| [ImageAttributes::Reset](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-reset.md) | The ImageAttributes |
| [ImageAttributes::SetBrushRemapTable](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setbrushremaptable.md) | The ImageAttributes |
| [ImageAttributes::SetColorKey](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setcolorkey.md) | The ImageAttributes |
| [ImageAttributes::SetColorMatrices](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setcolormatrices.md) | The ImageAttributes |
| [ImageAttributes::SetColorMatrix](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setcolormatrix.md) | The ImageAttributes |
| [ImageAttributes::SetGamma](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setgamma.md) | The ImageAttributes |
| [ImageAttributes::SetNoOp](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setnoop.md) | The ImageAttributes |
| [ImageAttributes::SetOutputChannelColorProfile](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setoutputchannelcolorprofile.md) | The ImageAttributes |
| [ImageAttributes::SetOutputChannel](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setoutputchannel.md) | The ImageAttributes |
| [ImageAttributes::SetRemapTable](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setremaptable.md) | The ImageAttributes |
| [ImageAttributes::SetThreshold](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setthreshold.md) | The ImageAttributes |
| [ImageAttributes::SetToIdentity](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-settoidentity.md) | The ImageAttributes |
| [ImageAttributes::SetWrapMode](..\gdiplusimageattributes\nf-gdiplusimageattributes-imageattributes-setwrapmode.md) | The ImageAttributes |
| [InstalledFontCollection::InstalledFontCollection(const InstalledFontCollection &)](..\gdiplusheaders\nf-gdiplusheaders-installedfontcollection-installedfontcollection(const installedfontcollection &).md) | Creates an InstalledFontCollection |
| [InstalledFontCollection::InstalledFontCollection](..\gdiplusheaders\nf-gdiplusheaders-installedfontcollection-installedfontcollection.md) | Creates an InstalledFontCollection |
| [Levels::GetParameters](..\gdipluseffects\nf-gdipluseffects-levels-getparameters.md) | The Levels |
| [Levels::Levels](..\gdipluseffects\nf-gdipluseffects-levels-levels.md) | Creates a Levels object. |
| [Levels::SetParameters](..\gdipluseffects\nf-gdipluseffects-levels-setparameters.md) | The Levels |
| [LinearGradientBrush::GetBlendCount](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-getblendcount.md) | The LinearGradientBrush |
| [LinearGradientBrush::GetBlend](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-getblend.md) | The LinearGradientBrush |
| [LinearGradientBrush::GetGammaCorrection](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-getgammacorrection.md) | The LinearGradientBrush |
| [LinearGradientBrush::GetInterpolationColorCount](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-getinterpolationcolorcount.md) | The LinearGradientBrush |
| [LinearGradientBrush::GetInterpolationColors](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-getinterpolationcolors.md) | The LinearGradientBrush |
| [LinearGradientBrush::GetLinearColors](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-getlinearcolors.md) | The LinearGradientBrush |
| [LinearGradientBrush::GetTransform](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-gettransform.md) | The LinearGradientBrush |
| [LinearGradientBrush::GetWrapMode](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-getwrapmode.md) | The LinearGradientBrush |
| [LinearGradientBrush::MultiplyTransform](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-multiplytransform.md) | The LinearGradientBrush |
| [LinearGradientBrush::ResetTransform](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-resettransform.md) | The LinearGradientBrush |
| [LinearGradientBrush::RotateTransform](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-rotatetransform.md) | The LinearGradientBrush |
| [LinearGradientBrush::ScaleTransform](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-scaletransform.md) | The LinearGradientBrush |
| [LinearGradientBrush::SetBlendBellShape](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-setblendbellshape.md) | The LinearGradientBrush |
| [LinearGradientBrush::SetBlendTriangularShape](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-setblendtriangularshape.md) | The LinearGradientBrush |
| [LinearGradientBrush::SetBlend](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-setblend.md) | The LinearGradientBrush |
| [LinearGradientBrush::SetGammaCorrection](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-setgammacorrection.md) | The LinearGradientBrush |
| [LinearGradientBrush::SetInterpolationColors](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-setinterpolationcolors.md) | The LinearGradientBrush |
| [LinearGradientBrush::SetLinearColors](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-setlinearcolors.md) | The LinearGradientBrush |
| [LinearGradientBrush::SetTransform](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-settransform.md) | The LinearGradientBrush |
| [LinearGradientBrush::SetWrapMode](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-setwrapmode.md) | The LinearGradientBrush |
| [LinearGradientBrush::TranslateTransform](..\gdiplusbrush\nf-gdiplusbrush-lineargradientbrush-translatetransform.md) | The LinearGradientBrush |
| [Matrix::Clone](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-clone.md) | The Matrix |
| [Matrix::Equals](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-equals.md) | The Matrix |
| [Matrix::GetElements](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-getelements.md) | The Matrix |
| [Matrix::GetLastStatus](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-getlaststatus.md) | The Matrix |
| [Matrix::Invert](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-invert.md) | If this matrix is invertible, the Matrix |
| [Matrix::IsIdentity](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-isidentity.md) | The Matrix |
| [Matrix::IsInvertible](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-isinvertible.md) | The Matrix |
| [Matrix::Matrix(GpMatrix)](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-matrix(gpmatrix).md) | Creates and initializes a Matrix |
| [Matrix::Matrix(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-matrix(in real,in real,in real,in real,in real,in real).md) | Creates and initializes a Matrix |
| [Matrix::Matrix(IN const Rect &,IN const Point)](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-matrix(in const rect &,in const point).md) | Creates and initializes a Matrix |
| [Matrix::Matrix(IN const RectF &,IN const PointF)](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-matrix(in const rectf &,in const pointf).md) | Creates and initializes a Matrix |
| [Matrix::Matrix(const Matrix &)](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-matrix(const matrix &).md) | Creates and initializes a Matrix |
| [Matrix::Matrix](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-matrix.md) | Creates and initializes a Matrix |
| [Matrix::Multiply](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-multiply.md) | The Matrix |
| [Matrix::OffsetX](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-offsetx.md) | The Matrix |
| [Matrix::OffsetY](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-offsety.md) | The Matrix |
| [Matrix::Reset](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-reset.md) | The Matrix |
| [Matrix::RotateAt](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-rotateat.md) | The Matrix |
| [Matrix::Rotate](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-rotate.md) | The Matrix |
| [Matrix::Scale](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-scale.md) | The Matrix |
| [Matrix::SetElements](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-setelements.md) | The Matrix |
| [Matrix::Shear](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-shear.md) | The Matrix |
| [Matrix::TransformVectors(IN OUT Point,IN INT)](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-transformvectors(in out point,in int).md) | This topic lists the TransformVectors methods of the Matrix class. For a complete list of methods for the Matrix class, see Matrix Methods. |
| [Matrix::TransformVectors](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-transformvectors.md) | This topic lists the TransformVectors methods of the Matrix class. For a complete list of methods for the Matrix class, see Matrix Methods. |
| [Matrix::Translate](..\gdiplusmatrix\nf-gdiplusmatrix-matrix-translate.md) | The Matrix |
| [MetafileHeader::GetBounds](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-getbounds.md) | The MetafileHeader |
| [MetafileHeader::GetDpiX](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-getdpix.md) | The MetafileHeader |
| [MetafileHeader::GetDpiY](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-getdpiy.md) | The MetafileHeader |
| [MetafileHeader::GetEmfHeader](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-getemfheader.md) | The MetafileHeader |
| [MetafileHeader::GetEmfPlusFlags](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-getemfplusflags.md) | The MetafileHeader |
| [MetafileHeader::GetMetafileSize](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-getmetafilesize.md) | The MetafileHeader |
| [MetafileHeader::GetType](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-gettype.md) | The MetafileHeader |
| [MetafileHeader::GetVersion](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-getversion.md) | The MetafileHeader |
| [MetafileHeader::GetWmfHeader](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-getwmfheader.md) | The MetafileHeader |
| [MetafileHeader::IsDisplay](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-isdisplay.md) | The MetafileHeader |
| [MetafileHeader::IsEmfOrEmfPlus](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-isemforemfplus.md) | The MetafileHeader |
| [MetafileHeader::IsEmfPlusDual](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-isemfplusdual.md) | The MetafileHeader |
| [MetafileHeader::IsEmfPlusOnly](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-isemfplusonly.md) | The MetafileHeader |
| [MetafileHeader::IsEmfPlus](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-isemfplus.md) | The MetafileHeader |
| [MetafileHeader::IsEmf](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-isemf.md) | The MetafileHeader |
| [MetafileHeader::IsWmfPlaceable](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-iswmfplaceable.md) | The MetafileHeader |
| [MetafileHeader::IsWmf](..\gdiplusmetaheader\nf-gdiplusmetaheader-metafileheader-iswmf.md) | The MetafileHeader |
| [PathData::PathData(const PathData &)](..\gdiplustypes\nf-gdiplustypes-pathdata-pathdata(const pathdata &).md) | Creates a PathData |
| [PathData::PathData](..\gdiplustypes\nf-gdiplustypes-pathdata-pathdata.md) | Creates a PathData |
| [PathGradientBrush::GetBlendCount](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getblendcount.md) | The PathGradientBrush |
| [PathGradientBrush::GetBlend](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getblend.md) | The PathGradientBrush |
| [PathGradientBrush::GetCenterColor](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getcentercolor.md) | The PathGradientBrush |
| [PathGradientBrush::GetFocusScales](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getfocusscales.md) | The PathGradientBrush |
| [PathGradientBrush::GetGammaCorrection](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getgammacorrection.md) | The PathGradientBrush |
| [PathGradientBrush::GetGraphicsPath](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getgraphicspath.md) | The PathGradientBrush |
| [PathGradientBrush::GetInterpolationColorCount](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getinterpolationcolorcount.md) | The PathGradientBrush |
| [PathGradientBrush::GetInterpolationColors](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getinterpolationcolors.md) | The PathGradientBrush |
| [PathGradientBrush::GetPointCount](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getpointcount.md) | The PathGradientBrush |
| [PathGradientBrush::GetSurroundColorCount](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getsurroundcolorcount.md) | The PathGradientBrush |
| [PathGradientBrush::GetSurroundColors](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getsurroundcolors.md) | The PathGradientBrush |
| [PathGradientBrush::GetTransform](..\gdipluspath\nf-gdipluspath-pathgradientbrush-gettransform.md) | The PathGradientBrush |
| [PathGradientBrush::GetWrapMode](..\gdipluspath\nf-gdipluspath-pathgradientbrush-getwrapmode.md) | The PathGradientBrush |
| [PathGradientBrush::MultiplyTransform](..\gdipluspath\nf-gdipluspath-pathgradientbrush-multiplytransform.md) | ThePathGradientBrush |
| [PathGradientBrush::ResetTransform](..\gdipluspath\nf-gdipluspath-pathgradientbrush-resettransform.md) | The PathGradientBrush |
| [PathGradientBrush::RotateTransform](..\gdipluspath\nf-gdipluspath-pathgradientbrush-rotatetransform.md) | The PathGradientBrush |
| [PathGradientBrush::ScaleTransform](..\gdipluspath\nf-gdipluspath-pathgradientbrush-scaletransform.md) | The PathGradientBrush |
| [PathGradientBrush::SetBlendBellShape](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setblendbellshape.md) | The PathGradientBrush |
| [PathGradientBrush::SetBlendTriangularShape](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setblendtriangularshape.md) | The PathGradientBrush |
| [PathGradientBrush::SetBlend](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setblend.md) | The PathGradientBrush |
| [PathGradientBrush::SetCenterColor](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setcentercolor.md) | The PathGradientBrush |
| [PathGradientBrush::SetCenterPoint(IN const Point &)](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setcenterpoint(in const point &).md) | This topic lists the SetCenterPoint methods of the PathGradientBrush class. For a complete list of methods for the PathGradientBrush class, see PathGradientBrush Methods. |
| [PathGradientBrush::SetCenterPoint](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setcenterpoint.md) | This topic lists the SetCenterPoint methods of the PathGradientBrush class. For a complete list of methods for the PathGradientBrush class, see PathGradientBrush Methods. |
| [PathGradientBrush::SetFocusScales](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setfocusscales.md) | The PathGradientBrush |
| [PathGradientBrush::SetGammaCorrection](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setgammacorrection.md) | The PathGradientBrush |
| [PathGradientBrush::SetGraphicsPath](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setgraphicspath.md) | The PathGradientBrush |
| [PathGradientBrush::SetInterpolationColors](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setinterpolationcolors.md) | The PathGradientBrush |
| [PathGradientBrush::SetSurroundColors](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setsurroundcolors.md) | The PathGradientBrush |
| [PathGradientBrush::SetTransform](..\gdipluspath\nf-gdipluspath-pathgradientbrush-settransform.md) | The PathGradientBrush |
| [PathGradientBrush::SetWrapMode](..\gdipluspath\nf-gdipluspath-pathgradientbrush-setwrapmode.md) | The PathGradientBrush |
| [PathGradientBrush::TranslateTransform](..\gdipluspath\nf-gdipluspath-pathgradientbrush-translatetransform.md) | The PathGradientBrush |
| [Pen::Clone](..\gdipluspen\nf-gdipluspen-pen-clone.md) | The Pen |
| [Pen::GetAlignment](..\gdipluspen\nf-gdipluspen-pen-getalignment.md) | The Pen |
| [Pen::GetBrush](..\gdipluspen\nf-gdipluspen-pen-getbrush.md) | The Pen |
| [Pen::GetColor](..\gdipluspen\nf-gdipluspen-pen-getcolor.md) | The Pen |
| [Pen::GetCompoundArrayCount](..\gdipluspen\nf-gdipluspen-pen-getcompoundarraycount.md) | The Pen |
| [Pen::GetCompoundArray](..\gdipluspen\nf-gdipluspen-pen-getcompoundarray.md) | The Pen |
| [Pen::GetCustomEndCap](..\gdipluspen\nf-gdipluspen-pen-getcustomendcap.md) | The Pen |
| [Pen::GetCustomStartCap](..\gdipluspen\nf-gdipluspen-pen-getcustomstartcap.md) | The Pen |
| [Pen::GetDashCap](..\gdipluspen\nf-gdipluspen-pen-getdashcap.md) | The Pen |
| [Pen::GetDashOffset](..\gdipluspen\nf-gdipluspen-pen-getdashoffset.md) | The Pen |
| [Pen::GetDashPatternCount](..\gdipluspen\nf-gdipluspen-pen-getdashpatterncount.md) | The Pen |
| [Pen::GetDashPattern](..\gdipluspen\nf-gdipluspen-pen-getdashpattern.md) | The Pen |
| [Pen::GetDashStyle](..\gdipluspen\nf-gdipluspen-pen-getdashstyle.md) | The Pen |
| [Pen::GetEndCap](..\gdipluspen\nf-gdipluspen-pen-getendcap.md) | The Pen |
| [Pen::GetLastStatus](..\gdipluspen\nf-gdipluspen-pen-getlaststatus.md) | The Pen |
| [Pen::GetLineJoin](..\gdipluspen\nf-gdipluspen-pen-getlinejoin.md) | The Pen |
| [Pen::GetMiterLimit](..\gdipluspen\nf-gdipluspen-pen-getmiterlimit.md) | The Pen |
| [Pen::GetPenType](..\gdipluspen\nf-gdipluspen-pen-getpentype.md) | The Pen |
| [Pen::GetStartCap](..\gdipluspen\nf-gdipluspen-pen-getstartcap.md) | The Pen |
| [Pen::GetTransform](..\gdipluspen\nf-gdipluspen-pen-gettransform.md) | The Pen |
| [Pen::GetWidth](..\gdipluspen\nf-gdipluspen-pen-getwidth.md) | The Pen |
| [Pen::MultiplyTransform](..\gdipluspen\nf-gdipluspen-pen-multiplytransform.md) | The Pen |
| [Pen::ResetTransform](..\gdipluspen\nf-gdipluspen-pen-resettransform.md) | The Pen |
| [Pen::RotateTransform](..\gdipluspen\nf-gdipluspen-pen-rotatetransform.md) | The Pen |
| [Pen::ScaleTransform](..\gdipluspen\nf-gdipluspen-pen-scaletransform.md) | The Pen |
| [Pen::SetAlignment](..\gdipluspen\nf-gdipluspen-pen-setalignment.md) | The Pen |
| [Pen::SetBrush](..\gdipluspen\nf-gdipluspen-pen-setbrush.md) | The Pen |
| [Pen::SetColor](..\gdipluspen\nf-gdipluspen-pen-setcolor.md) | The Pen |
| [Pen::SetCompoundArray](..\gdipluspen\nf-gdipluspen-pen-setcompoundarray.md) | The Pen |
| [Pen::SetCustomEndCap](..\gdipluspen\nf-gdipluspen-pen-setcustomendcap.md) | The Pen |
| [Pen::SetCustomStartCap](..\gdipluspen\nf-gdipluspen-pen-setcustomstartcap.md) | The Pen |
| [Pen::SetDashCap](..\gdipluspen\nf-gdipluspen-pen-setdashcap.md) | The Pen |
| [Pen::SetDashOffset](..\gdipluspen\nf-gdipluspen-pen-setdashoffset.md) | The Pen |
| [Pen::SetDashPattern](..\gdipluspen\nf-gdipluspen-pen-setdashpattern.md) | The Pen |
| [Pen::SetDashStyle](..\gdipluspen\nf-gdipluspen-pen-setdashstyle.md) | The Pen |
| [Pen::SetEndCap](..\gdipluspen\nf-gdipluspen-pen-setendcap.md) | The Pen |
| [Pen::SetLineCap](..\gdipluspen\nf-gdipluspen-pen-setlinecap.md) | The Pen |
| [Pen::SetLineJoin](..\gdipluspen\nf-gdipluspen-pen-setlinejoin.md) | The Pen |
| [Pen::SetMiterLimit](..\gdipluspen\nf-gdipluspen-pen-setmiterlimit.md) | The Pen |
| [Pen::SetStartCap](..\gdipluspen\nf-gdipluspen-pen-setstartcap.md) | The Pen |
| [Pen::SetTransform](..\gdipluspen\nf-gdipluspen-pen-settransform.md) | The Pen |
| [Pen::SetWidth](..\gdipluspen\nf-gdipluspen-pen-setwidth.md) | The Pen |
| [Point::Equals](..\gdiplustypes\nf-gdiplustypes-point-equals.md) | The Point |
| [Point::Point(IN INT,IN INT)](..\gdiplustypes\nf-gdiplustypes-point-point(in int,in int).md) | Creates a Point object and initializes the X and Y data members to zero. This is the default constructor. |
| [Point::Point(IN const Point &)](..\gdiplustypes\nf-gdiplustypes-point-point(in const point &).md) | Creates a Point object and initializes the X and Y data members to zero. This is the default constructor. |
| [Point::Point(IN const Size &)](..\gdiplustypes\nf-gdiplustypes-point-point(in const size &).md) | Creates a Point object and initializes the X and Y data members to zero. This is the default constructor. |
| [Point::Point](..\gdiplustypes\nf-gdiplustypes-point-point.md) | Creates a Point object and initializes the X and Y data members to zero. This is the default constructor. |
| [PointF::Equals](..\gdiplustypes\nf-gdiplustypes-pointf-equals.md) | The PointF |
| [PointF::PointF(IN REAL,IN REAL)](..\gdiplustypes\nf-gdiplustypes-pointf-pointf(in real,in real).md) | Creates a PointF object and initializes the X and Y data members to zero. This is the default constructor. |
| [PointF::PointF(IN const PointF &)](..\gdiplustypes\nf-gdiplustypes-pointf-pointf(in const pointf &).md) | Creates a PointF object and initializes the X and Y data members to zero. This is the default constructor. |
| [PointF::PointF(IN const SizeF &)](..\gdiplustypes\nf-gdiplustypes-pointf-pointf(in const sizef &).md) | Creates a PointF object and initializes the X and Y data members to zero. This is the default constructor. |
| [PointF::PointF](..\gdiplustypes\nf-gdiplustypes-pointf-pointf.md) | Creates a PointF object and initializes the X and Y data members to zero. This is the default constructor. |
| [PrivateFontCollection::AddFontFile](..\gdiplusheaders\nf-gdiplusheaders-privatefontcollection-addfontfile.md) | The PrivateFontCollection |
| [PrivateFontCollection::AddMemoryFont](..\gdiplusheaders\nf-gdiplusheaders-privatefontcollection-addmemoryfont.md) | The PrivateFontCollection |
| [PrivateFontCollection::PrivateFontCollection(const PrivateFontCollection &)](..\gdiplusheaders\nf-gdiplusheaders-privatefontcollection-privatefontcollection(const privatefontcollection &).md) | Creates an empty PrivateFontCollection object. |
| [PrivateFontCollection::PrivateFontCollection](..\gdiplusheaders\nf-gdiplusheaders-privatefontcollection-privatefontcollection.md) | Creates an empty PrivateFontCollection object. |
| [Rect::Clone](..\gdiplustypes\nf-gdiplustypes-rect-clone.md) | The Rect |
| [Rect::Equals](..\gdiplustypes\nf-gdiplustypes-rect-equals.md) | The Rect |
| [Rect::GetBottom](..\gdiplustypes\nf-gdiplustypes-rect-getbottom.md) | The Rect |
| [Rect::GetBounds](..\gdiplustypes\nf-gdiplustypes-rect-getbounds.md) | The Rect |
| [Rect::GetLeft](..\gdiplustypes\nf-gdiplustypes-rect-getleft.md) | The Rect |
| [Rect::GetLocation](..\gdiplustypes\nf-gdiplustypes-rect-getlocation.md) | The Rect |
| [Rect::GetRight](..\gdiplustypes\nf-gdiplustypes-rect-getright.md) | The Rect |
| [Rect::GetSize](..\gdiplustypes\nf-gdiplustypes-rect-getsize.md) | The Rect |
| [Rect::GetTop](..\gdiplustypes\nf-gdiplustypes-rect-gettop.md) | The Rect |
| [Rect::Inflate(IN const Point &)](..\gdiplustypes\nf-gdiplustypes-rect-inflate(in const point &).md) | This topic lists the Inflate methods of the Rect class. For a complete list of methods for the Rect class, see Rect Methods. |
| [Rect::Inflate](..\gdiplustypes\nf-gdiplustypes-rect-inflate.md) | This topic lists the Inflate methods of the Rect class. For a complete list of methods for the Rect class, see Rect Methods. |
| [Rect::IntersectsWith](..\gdiplustypes\nf-gdiplustypes-rect-intersectswith.md) | The Rect |
| [Rect::IsEmptyArea](..\gdiplustypes\nf-gdiplustypes-rect-isemptyarea.md) | The Rect |
| [Rect::Rect(IN INT,IN INT,IN INT,IN INT)](..\gdiplustypes\nf-gdiplustypes-rect-rect(in int,in int,in int,in int).md) | Creates a Rect object whose x-coordinate, y-coordinate, width, and height are all zero. This is the default constructor. |
| [Rect::Rect(IN const Point &,IN const Size &)](..\gdiplustypes\nf-gdiplustypes-rect-rect(in const point &,in const size &).md) | Creates a Rect object whose x-coordinate, y-coordinate, width, and height are all zero. This is the default constructor. |
| [Rect::Rect](..\gdiplustypes\nf-gdiplustypes-rect-rect.md) | Creates a Rect object whose x-coordinate, y-coordinate, width, and height are all zero. This is the default constructor. |
| [Rect::Union](..\gdiplustypes\nf-gdiplustypes-rect-union.md) | The Rect |
| [RectF::Clone](..\gdiplustypes\nf-gdiplustypes-rectf-clone.md) | The RectF |
| [RectF::Equals](..\gdiplustypes\nf-gdiplustypes-rectf-equals.md) | The RectF |
| [RectF::GetBottom](..\gdiplustypes\nf-gdiplustypes-rectf-getbottom.md) | The RectF |
| [RectF::GetBounds](..\gdiplustypes\nf-gdiplustypes-rectf-getbounds.md) | The RectF |
| [RectF::GetLeft](..\gdiplustypes\nf-gdiplustypes-rectf-getleft.md) | The RectF |
| [RectF::GetLocation](..\gdiplustypes\nf-gdiplustypes-rectf-getlocation.md) | The RectF |
| [RectF::GetRight](..\gdiplustypes\nf-gdiplustypes-rectf-getright.md) | The RectF |
| [RectF::GetSize](..\gdiplustypes\nf-gdiplustypes-rectf-getsize.md) | The RectF |
| [RectF::GetTop](..\gdiplustypes\nf-gdiplustypes-rectf-gettop.md) | The RectF |
| [RectF::Inflate(IN const PointF &)](..\gdiplustypes\nf-gdiplustypes-rectf-inflate(in const pointf &).md) | This topic lists the Inflate methods of the RectF class. For a complete list of methods for the RectF class, see RectF Methods. |
| [RectF::Inflate](..\gdiplustypes\nf-gdiplustypes-rectf-inflate.md) | This topic lists the Inflate methods of the RectF class. For a complete list of methods for the RectF class, see RectF Methods. |
| [RectF::IntersectsWith](..\gdiplustypes\nf-gdiplustypes-rectf-intersectswith.md) | The RectF |
| [RectF::IsEmptyArea](..\gdiplustypes\nf-gdiplustypes-rectf-isemptyarea.md) | The RectF |
| [RectF::RectF(IN REAL,IN REAL,IN REAL,IN REAL)](..\gdiplustypes\nf-gdiplustypes-rectf-rectf(in real,in real,in real,in real).md) | Creates a RectF object and initializes the X, Y, Width, and Height data members to zero. This is the default constructor. |
| [RectF::RectF(IN const PointF &,IN const SizeF &)](..\gdiplustypes\nf-gdiplustypes-rectf-rectf(in const pointf &,in const sizef &).md) | Creates a RectF object and initializes the X, Y, Width, and Height data members to zero. This is the default constructor. |
| [RectF::RectF](..\gdiplustypes\nf-gdiplustypes-rectf-rectf.md) | Creates a RectF object and initializes the X, Y, Width, and Height data members to zero. This is the default constructor. |
| [RectF::Union](..\gdiplustypes\nf-gdiplustypes-rectf-union.md) | The RectF |
| [RedEyeCorrection::GetParameters](..\gdipluseffects\nf-gdipluseffects-redeyecorrection-getparameters.md) | The RedEyeCorrection |
| [RedEyeCorrection::RedEyeCorrection](..\gdipluseffects\nf-gdipluseffects-redeyecorrection-redeyecorrection.md) | Creates a RedEyeCorrection object. |
| [RedEyeCorrection::SetParameters](..\gdipluseffects\nf-gdipluseffects-redeyecorrection-setparameters.md) | The RedEyeCorrection |
| [Region::Clone](..\gdiplusheaders\nf-gdiplusheaders-region-clone.md) | The Region |
| [Region::Equals](..\gdiplusheaders\nf-gdiplusheaders-region-equals.md) | The Region |
| [Region::FromHRGN](..\gdiplusheaders\nf-gdiplusheaders-region-fromhrgn.md) | The Region |
| [Region::GetDataSize](..\gdiplusheaders\nf-gdiplusheaders-region-getdatasize.md) | The Region |
| [Region::GetData](..\gdiplusheaders\nf-gdiplusheaders-region-getdata.md) | The Region |
| [Region::GetHRGN](..\gdiplusheaders\nf-gdiplusheaders-region-gethrgn.md) | The Region |
| [Region::GetLastStatus](..\gdiplusheaders\nf-gdiplusheaders-region-getlaststatus.md) | The Region |
| [Region::GetRegionScansCount](..\gdiplusheaders\nf-gdiplusheaders-region-getregionscanscount.md) | The Region |
| [Region::IsEmpty](..\gdiplusheaders\nf-gdiplusheaders-region-isempty.md) | The Region |
| [Region::IsInfinite](..\gdiplusheaders\nf-gdiplusheaders-region-isinfinite.md) | The Region |
| [Region::MakeEmpty](..\gdiplusheaders\nf-gdiplusheaders-region-makeempty.md) | The Region |
| [Region::MakeInfinite](..\gdiplusheaders\nf-gdiplusheaders-region-makeinfinite.md) | The Region |
| [Region::Region(GpRegion)](..\gdiplusheaders\nf-gdiplusheaders-region-region(gpregion).md) | Creates a region that is infinite. This is the default constructor. |
| [Region::Region(IN HRGN)](..\gdiplusheaders\nf-gdiplusheaders-region-region(in hrgn).md) | Creates a region that is infinite. This is the default constructor. |
| [Region::Region(IN const BYTE,IN INT)](..\gdiplusheaders\nf-gdiplusheaders-region-region(in const byte,in int).md) | Creates a region that is infinite. This is the default constructor. |
| [Region::Region(IN const GraphicsPath)](..\gdiplusheaders\nf-gdiplusheaders-region-region(in const graphicspath).md) | Creates a region that is infinite. This is the default constructor. |
| [Region::Region(IN const Rect &)](..\gdiplusheaders\nf-gdiplusheaders-region-region(in const rect &).md) | Creates a region that is infinite. This is the default constructor. |
| [Region::Region(IN const RectF &)](..\gdiplusheaders\nf-gdiplusheaders-region-region(in const rectf &).md) | Creates a region that is infinite. This is the default constructor. |
| [Region::Region(const Region &)](..\gdiplusheaders\nf-gdiplusheaders-region-region(const region &).md) | Creates a region that is infinite. This is the default constructor. |
| [Region::Region](..\gdiplusheaders\nf-gdiplusheaders-region-region.md) | Creates a region that is infinite. This is the default constructor. |
| [Region::Transform](..\gdiplusheaders\nf-gdiplusheaders-region-transform.md) | The Region |
| [Sharpen::GetParameters](..\gdipluseffects\nf-gdipluseffects-sharpen-getparameters.md) | The Sharpen |
| [Sharpen::SetParameters](..\gdipluseffects\nf-gdipluseffects-sharpen-setparameters.md) | The Sharpen |
| [Sharpen::Sharpen](..\gdipluseffects\nf-gdipluseffects-sharpen-sharpen.md) | Creates a Sharpen object. |
| [Size::Empty](..\gdiplustypes\nf-gdiplustypes-size-empty.md) | The Size |
| [Size::Equals](..\gdiplustypes\nf-gdiplustypes-size-equals.md) | The Size |
| [Size::Size(IN INT,IN INT)](..\gdiplustypes\nf-gdiplustypes-size-size(in int,in int).md) | Creates a new Size object and initializes the members to zero. This is the default constructor. |
| [Size::Size(IN const Size &)](..\gdiplustypes\nf-gdiplustypes-size-size(in const size &).md) | Creates a new Size object and initializes the members to zero. This is the default constructor. |
| [Size::Size](..\gdiplustypes\nf-gdiplustypes-size-size.md) | Creates a new Size object and initializes the members to zero. This is the default constructor. |
| [SizeF::Empty](..\gdiplustypes\nf-gdiplustypes-sizef-empty.md) | The SizeF |
| [SizeF::Equals](..\gdiplustypes\nf-gdiplustypes-sizef-equals.md) | The SizeF |
| [SizeF::SizeF(IN REAL,IN REAL)](..\gdiplustypes\nf-gdiplustypes-sizef-sizef(in real,in real).md) | Creates a SizeF object and initializes the members to zero. This is the default constructor. |
| [SizeF::SizeF(IN const SizeF &)](..\gdiplustypes\nf-gdiplustypes-sizef-sizef(in const sizef &).md) | Creates a SizeF object and initializes the members to zero. This is the default constructor. |
| [SizeF::SizeF](..\gdiplustypes\nf-gdiplustypes-sizef-sizef.md) | Creates a SizeF object and initializes the members to zero. This is the default constructor. |
| [SolidBrush::GetColor](..\gdiplusbrush\nf-gdiplusbrush-solidbrush-getcolor.md) | The SolidBrush |
| [SolidBrush::SetColor](..\gdiplusbrush\nf-gdiplusbrush-solidbrush-setcolor.md) | The SolidBrush |
| [SolidBrush::SolidBrush(IN const Color &)](..\gdiplusbrush\nf-gdiplusbrush-solidbrush-solidbrush(in const color &).md) | Creates a SolidBrush object based on a color. |
| [SolidBrush::SolidBrush(const SolidBrush &)](..\gdiplusbrush\nf-gdiplusbrush-solidbrush-solidbrush(const solidbrush &).md) | Creates a SolidBrush object based on a color. |
| [SolidBrush::SolidBrush~r3](..\gdiplusbrush\nf-gdiplusbrush-solidbrush-solidbrush~r3.md) | Creates a SolidBrush object based on a color. |
| [StringFormat::Clone](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-clone.md) | The StringFormat |
| [StringFormat::GenericDefault](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-genericdefault.md) | The StringFormat |
| [StringFormat::GenericTypographic](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-generictypographic.md) | The StringFormat |
| [StringFormat::GetAlignment](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-getalignment.md) | The StringFormat |
| [StringFormat::GetDigitSubstitutionLanguage](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-getdigitsubstitutionlanguage.md) | The StringFormat |
| [StringFormat::GetDigitSubstitutionMethod](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-getdigitsubstitutionmethod.md) | The StringFormat |
| [StringFormat::GetFormatFlags](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-getformatflags.md) | The StringFormat |
| [StringFormat::GetHotkeyPrefix](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-gethotkeyprefix.md) | The StringFormat |
| [StringFormat::GetLastStatus](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-getlaststatus.md) | The StringFormat |
| [StringFormat::GetLineAlignment](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-getlinealignment.md) | The StringFormat |
| [StringFormat::GetMeasurableCharacterRangeCount](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-getmeasurablecharacterrangecount.md) | The StringFormat |
| [StringFormat::GetTabStopCount](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-gettabstopcount.md) | The StringFormat |
| [StringFormat::GetTabStops](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-gettabstops.md) | The StringFormat |
| [StringFormat::GetTrimming](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-gettrimming.md) | The StringFormat |
| [StringFormat::SetAlignment](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-setalignment.md) | The StringFormat |
| [StringFormat::SetDigitSubstitution](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-setdigitsubstitution.md) | The StringFormat |
| [StringFormat::SetFormatFlags](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-setformatflags.md) | The StringFormat |
| [StringFormat::SetHotkeyPrefix](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-sethotkeyprefix.md) | The StringFormat |
| [StringFormat::SetLineAlignment](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-setlinealignment.md) | The StringFormat |
| [StringFormat::SetMeasurableCharacterRanges](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-setmeasurablecharacterranges.md) | The StringFormat |
| [StringFormat::SetTabStops](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-settabstops.md) | The StringFormat |
| [StringFormat::SetTrimming](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-settrimming.md) | The StringFormat |
| [StringFormat::StringFormat(GpStringFormat,Status)](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-stringformat(gpstringformat,status).md) | This topic lists the constructors of the StringFormat class. For a complete class listing, see StringFormat Class. |
| [StringFormat::StringFormat(IN INT,IN LANGID)](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-stringformat(in int,in langid).md) | This topic lists the constructors of the StringFormat class. For a complete class listing, see StringFormat Class. |
| [StringFormat::StringFormat(IN const StringFormat)](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-stringformat(in const stringformat).md) | This topic lists the constructors of the StringFormat class. For a complete class listing, see StringFormat Class. |
| [StringFormat::StringFormat(const StringFormat &)](..\gdiplusstringformat\nf-gdiplusstringformat-stringformat-stringformat(const stringformat &).md) | This topic lists the constructors of the StringFormat class. For a complete class listing, see StringFormat Class. |
| [TextureBrush::GetImage](..\gdiplusbrush\nf-gdiplusbrush-texturebrush-getimage.md) | The TextureBrush |
| [TextureBrush::GetTransform](..\gdiplusbrush\nf-gdiplusbrush-texturebrush-gettransform.md) | The TextureBrush |
| [TextureBrush::GetWrapMode](..\gdiplusbrush\nf-gdiplusbrush-texturebrush-getwrapmode.md) | The TextureBrush |
| [TextureBrush::MultiplyTransform](..\gdiplusbrush\nf-gdiplusbrush-texturebrush-multiplytransform.md) | The TextureBrush |
| [TextureBrush::ResetTransform](..\gdiplusbrush\nf-gdiplusbrush-texturebrush-resettransform.md) | The TextureBrush |
| [TextureBrush::RotateTransform](..\gdiplusbrush\nf-gdiplusbrush-texturebrush-rotatetransform.md) | The TextureBrush |
| [TextureBrush::ScaleTransform](..\gdiplusbrush\nf-gdiplusbrush-texturebrush-scaletransform.md) | The TextureBrush |
| [TextureBrush::SetTransform](..\gdiplusbrush\nf-gdiplusbrush-texturebrush-settransform.md) | The TextureBrush |
| [TextureBrush::SetWrapMode](..\gdiplusbrush\nf-gdiplusbrush-texturebrush-setwrapmode.md) | The TextureBrush |
| [TextureBrush::TranslateTransform](..\gdiplusbrush\nf-gdiplusbrush-texturebrush-translatetransform.md) | The TextureBrush |
| [Tint::GetParameters](..\gdipluseffects\nf-gdipluseffects-tint-getparameters.md) | The Tint |
| [Tint::SetParameters](..\gdipluseffects\nf-gdipluseffects-tint-setparameters.md) | The Tint |
| [Tint::Tint](..\gdipluseffects\nf-gdipluseffects-tint-tint.md) | Creates a Tint object. |
