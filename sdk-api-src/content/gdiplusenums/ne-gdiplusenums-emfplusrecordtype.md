---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# EmfPlusRecordType enumeration


## -description


The <b>EmfPlusRecordType</b> enumeration identifies metafile record types used in Windows Metafile Format (WMF), Enhanced Metafile (EMF), and EMF+ files. The elements of the <b>EmfPlusRecordType</b> enumeration come in three groups.
<ul>
<li>Elements in the first group have the prefix WmfRecordType and identity WMF records.</li>
<li>Elements in the second group have the prefix EmfRecordType and identify EMF records.</li>
<li>Elements in the third group have the prefix EmfPlusRecordType and identify EMF+ records.</li>
</ul>WMF and EMF records can be displayed by Windows GDI+ and by Windows Graphics Device Interface (GDI). EMF+ records can be displayed by GDI+ but not by GDI.

Elements that have the WmfRecordType prefix are analogous to constants (defined in Wingdi.h) that have the prefix META_. For example, the element <b><b>WmfRecordTypeSetBkColor</b></b> is analogous to the constant META_SETBKCOLOR. For more information about WMF files, see <a href="https://msdn.microsoft.com/ebbf871b-cf78-4a90-8f27-e44699c17178">Windows-Format Metafiles</a>.

Elements that have the EmfRecordType prefix are analogous to constants (defined in Wingdi.h) that have the prefix EMR_. For example, the element <b><b>EmfRecordTypePolygon</b></b> is analogous to the constant EMR_POLYGON. For more information about EMR constants, see <a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>.

Elements that have the EmfPlusRecordType prefix are specific to GDI+. Most of those elements correspond to methods of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> class. The remaining elements identify the header, the end of the file, and other sections of the metafile. The Constants section of this topic shows the correspondence between the EMF+ record types and the methods of the <b>Graphics</b> class.


## -enum-fields




### -field WmfRecordTypeSetBkColor


### -field WmfRecordTypeSetBkMode


### -field WmfRecordTypeSetMapMode


### -field WmfRecordTypeSetROP2


### -field WmfRecordTypeSetRelAbs


### -field WmfRecordTypeSetPolyFillMode


### -field WmfRecordTypeSetStretchBltMode


### -field WmfRecordTypeSetTextCharExtra


### -field WmfRecordTypeSetTextColor


### -field WmfRecordTypeSetTextJustification


### -field WmfRecordTypeSetWindowOrg


### -field WmfRecordTypeSetWindowExt


### -field WmfRecordTypeSetViewportOrg


### -field WmfRecordTypeSetViewportExt


### -field WmfRecordTypeOffsetWindowOrg


### -field WmfRecordTypeScaleWindowExt


### -field WmfRecordTypeOffsetViewportOrg


### -field WmfRecordTypeScaleViewportExt


### -field WmfRecordTypeLineTo


### -field WmfRecordTypeMoveTo


### -field WmfRecordTypeExcludeClipRect


### -field WmfRecordTypeIntersectClipRect


### -field WmfRecordTypeArc


### -field WmfRecordTypeEllipse


### -field WmfRecordTypeFloodFill


### -field WmfRecordTypePie


### -field WmfRecordTypeRectangle


### -field WmfRecordTypeRoundRect


### -field WmfRecordTypePatBlt


### -field WmfRecordTypeSaveDC


### -field WmfRecordTypeSetPixel


### -field WmfRecordTypeOffsetClipRgn


### -field WmfRecordTypeTextOut


### -field WmfRecordTypeBitBlt


### -field WmfRecordTypeStretchBlt


### -field WmfRecordTypePolygon


### -field WmfRecordTypePolyline


### -field WmfRecordTypeEscape


### -field WmfRecordTypeRestoreDC


### -field WmfRecordTypeFillRegion


### -field WmfRecordTypeFrameRegion


### -field WmfRecordTypeInvertRegion


### -field WmfRecordTypePaintRegion


### -field WmfRecordTypeSelectClipRegion


### -field WmfRecordTypeSelectObject


### -field WmfRecordTypeSetTextAlign


### -field WmfRecordTypeDrawText


### -field WmfRecordTypeChord


### -field WmfRecordTypeSetMapperFlags


### -field WmfRecordTypeExtTextOut


### -field WmfRecordTypeSetDIBToDev


### -field WmfRecordTypeSelectPalette


### -field WmfRecordTypeRealizePalette


### -field WmfRecordTypeAnimatePalette


### -field WmfRecordTypeSetPalEntries


### -field WmfRecordTypePolyPolygon


### -field WmfRecordTypeResizePalette


### -field WmfRecordTypeDIBBitBlt


### -field WmfRecordTypeDIBStretchBlt


### -field WmfRecordTypeDIBCreatePatternBrush


### -field WmfRecordTypeStretchDIB


### -field WmfRecordTypeExtFloodFill


### -field WmfRecordTypeSetLayout


### -field WmfRecordTypeResetDC


### -field WmfRecordTypeStartDoc


### -field WmfRecordTypeStartPage


### -field WmfRecordTypeEndPage


### -field WmfRecordTypeAbortDoc


### -field WmfRecordTypeEndDoc


### -field WmfRecordTypeDeleteObject


### -field WmfRecordTypeCreatePalette


### -field WmfRecordTypeCreateBrush


### -field WmfRecordTypeCreatePatternBrush


### -field WmfRecordTypeCreatePenIndirect


### -field WmfRecordTypeCreateFontIndirect


### -field WmfRecordTypeCreateBrushIndirect


### -field WmfRecordTypeCreateBitmapIndirect


### -field WmfRecordTypeCreateBitmap


### -field WmfRecordTypeCreateRegion


### -field EmfRecordTypeHeader


### -field EmfRecordTypePolyBezier


### -field EmfRecordTypePolygon


### -field EmfRecordTypePolyline


### -field EmfRecordTypePolyBezierTo


### -field EmfRecordTypePolyLineTo


### -field EmfRecordTypePolyPolyline


### -field EmfRecordTypePolyPolygon


### -field EmfRecordTypeSetWindowExtEx


### -field EmfRecordTypeSetWindowOrgEx


### -field EmfRecordTypeSetViewportExtEx


### -field EmfRecordTypeSetViewportOrgEx


### -field EmfRecordTypeSetBrushOrgEx


### -field EmfRecordTypeEOF


### -field EmfRecordTypeSetPixelV


### -field EmfRecordTypeSetMapperFlags


### -field EmfRecordTypeSetMapMode


### -field EmfRecordTypeSetBkMode


### -field EmfRecordTypeSetPolyFillMode


### -field EmfRecordTypeSetROP2


### -field EmfRecordTypeSetStretchBltMode


### -field EmfRecordTypeSetTextAlign


### -field EmfRecordTypeSetColorAdjustment


### -field EmfRecordTypeSetTextColor


### -field EmfRecordTypeSetBkColor


### -field EmfRecordTypeOffsetClipRgn


### -field EmfRecordTypeMoveToEx


### -field EmfRecordTypeSetMetaRgn


### -field EmfRecordTypeExcludeClipRect


### -field EmfRecordTypeIntersectClipRect


### -field EmfRecordTypeScaleViewportExtEx


### -field EmfRecordTypeScaleWindowExtEx


### -field EmfRecordTypeSaveDC


### -field EmfRecordTypeRestoreDC


### -field EmfRecordTypeSetWorldTransform


### -field EmfRecordTypeModifyWorldTransform


### -field EmfRecordTypeSelectObject


### -field EmfRecordTypeCreatePen


### -field EmfRecordTypeCreateBrushIndirect


### -field EmfRecordTypeDeleteObject


### -field EmfRecordTypeAngleArc


### -field EmfRecordTypeEllipse


### -field EmfRecordTypeRectangle


### -field EmfRecordTypeRoundRect


### -field EmfRecordTypeArc


### -field EmfRecordTypeChord


### -field EmfRecordTypePie


### -field EmfRecordTypeSelectPalette


### -field EmfRecordTypeCreatePalette


### -field EmfRecordTypeSetPaletteEntries


### -field EmfRecordTypeResizePalette


### -field EmfRecordTypeRealizePalette


### -field EmfRecordTypeExtFloodFill


### -field EmfRecordTypeLineTo


### -field EmfRecordTypeArcTo


### -field EmfRecordTypePolyDraw


### -field EmfRecordTypeSetArcDirection


### -field EmfRecordTypeSetMiterLimit


### -field EmfRecordTypeBeginPath


### -field EmfRecordTypeEndPath


### -field EmfRecordTypeCloseFigure


### -field EmfRecordTypeFillPath


### -field EmfRecordTypeStrokeAndFillPath


### -field EmfRecordTypeStrokePath


### -field EmfRecordTypeFlattenPath


### -field EmfRecordTypeWidenPath


### -field EmfRecordTypeSelectClipPath


### -field EmfRecordTypeAbortPath


### -field EmfRecordTypeReserved_069


### -field EmfRecordTypeGdiComment


### -field EmfRecordTypeFillRgn


### -field EmfRecordTypeFrameRgn


### -field EmfRecordTypeInvertRgn


### -field EmfRecordTypePaintRgn


### -field EmfRecordTypeExtSelectClipRgn


### -field EmfRecordTypeBitBlt


### -field EmfRecordTypeStretchBlt


### -field EmfRecordTypeMaskBlt


### -field EmfRecordTypePlgBlt


### -field EmfRecordTypeSetDIBitsToDevice


### -field EmfRecordTypeStretchDIBits


### -field EmfRecordTypeExtCreateFontIndirect


### -field EmfRecordTypeExtTextOutA


### -field EmfRecordTypeExtTextOutW


### -field EmfRecordTypePolyBezier16


### -field EmfRecordTypePolygon16


### -field EmfRecordTypePolyline16


### -field EmfRecordTypePolyBezierTo16


### -field EmfRecordTypePolylineTo16


### -field EmfRecordTypePolyPolyline16


### -field EmfRecordTypePolyPolygon16


### -field EmfRecordTypePolyDraw16


### -field EmfRecordTypeCreateMonoBrush


### -field EmfRecordTypeCreateDIBPatternBrushPt


### -field EmfRecordTypeExtCreatePen


### -field EmfRecordTypePolyTextOutA


### -field EmfRecordTypePolyTextOutW


### -field EmfRecordTypeSetICMMode


### -field EmfRecordTypeCreateColorSpace


### -field EmfRecordTypeSetColorSpace


### -field EmfRecordTypeDeleteColorSpace


### -field EmfRecordTypeGLSRecord


### -field EmfRecordTypeGLSBoundedRecord


### -field EmfRecordTypePixelFormat


### -field EmfRecordTypeDrawEscape


### -field EmfRecordTypeExtEscape


### -field EmfRecordTypeStartDoc


### -field EmfRecordTypeSmallTextOut


### -field EmfRecordTypeForceUFIMapping


### -field EmfRecordTypeNamedEscape


### -field EmfRecordTypeColorCorrectPalette


### -field EmfRecordTypeSetICMProfileA


### -field EmfRecordTypeSetICMProfileW


### -field EmfRecordTypeAlphaBlend


### -field EmfRecordTypeSetLayout


### -field EmfRecordTypeTransparentBlt


### -field EmfRecordTypeReserved_117


### -field EmfRecordTypeGradientFill


### -field EmfRecordTypeSetLinkedUFIs


### -field EmfRecordTypeSetTextJustification


### -field EmfRecordTypeColorMatchToTargetW


### -field EmfRecordTypeCreateColorSpaceW


### -field EmfRecordTypeMax


### -field EmfRecordTypeMin


### -field EmfPlusRecordTypeInvalid


### -field EmfPlusRecordTypeHeader

Identifies a record that is the EMF+ header.


### -field EmfPlusRecordTypeEndOfFile

Identifies a record that marks the last EMF+ record of a metafile.


### -field EmfPlusRecordTypeComment


<a href="https://msdn.microsoft.com/839b6918-1656-46ae-9bfd-85305306715c">Graphics::AddMetafileComment</a>



### -field EmfPlusRecordTypeGetDC


<a href="https://msdn.microsoft.com/b1a81c8b-7968-4ad8-a7b6-ebe6c266fd0b">Graphics::GetHDC</a>



### -field EmfPlusRecordTypeMultiFormatStart

Identifies the start of a multiple-format block.


### -field EmfPlusRecordTypeMultiFormatSection

Identifies a section in a multiple-format block. Multiple-format records allow the same set of records to be represented in several formats.


### -field EmfPlusRecordTypeMultiFormatEnd

Identifies the end of a multiple-format block.


### -field EmfPlusRecordTypeObject


### -field EmfPlusRecordTypeClear


<a href="https://msdn.microsoft.com/b59b72ff-8c7a-43f2-98ec-067f95325e1e">Graphics::Clear</a>



### -field EmfPlusRecordTypeFillRects


<a href="https://msdn.microsoft.com/705d1728-5742-4ed0-bea3-651b3ba40b40">FillRectangles Methods</a>



### -field EmfPlusRecordTypeDrawRects


<a href="https://msdn.microsoft.com/1c0c0e09-2304-4d68-9dd0-22b0861a2492">DrawRectangles Methods</a>



### -field EmfPlusRecordTypeFillPolygon


<a href="https://msdn.microsoft.com/e7cc93ab-c1e6-40e7-8888-f6bbffa42a00">FillPolygon Methods</a>



### -field EmfPlusRecordTypeDrawLines


<a href="https://msdn.microsoft.com/dc82feef-7d03-45dd-a949-42589511b177">DrawLines Methods</a>



### -field EmfPlusRecordTypeFillEllipse


<a href="https://msdn.microsoft.com/92f6f3ca-337b-4f57-9472-2dc677550b39">FillEllipse Methods</a>



### -field EmfPlusRecordTypeDrawEllipse


<a href="https://msdn.microsoft.com/1abaee7d-63a5-4786-b08c-f3b59e50f180">DrawEllipse Methods</a>



### -field EmfPlusRecordTypeFillPie


<a href="https://msdn.microsoft.com/e6de6634-b87f-4fe9-a0d4-ffeea0e0ae8b">FillPie Methods</a>



### -field EmfPlusRecordTypeDrawPie


<a href="https://msdn.microsoft.com/4c6b363f-ffe4-4572-98c0-55f84f789b1e">DrawPie Methods</a>



### -field EmfPlusRecordTypeDrawArc


<a href="https://msdn.microsoft.com/b30757ea-b8b8-45bd-a716-a4c8c9c5f1ec">DrawArc Methods</a>



### -field EmfPlusRecordTypeFillRegion


<a href="https://msdn.microsoft.com/000ac0f9-0963-46b6-a64d-f3cfb06e3eb9">Graphics::FillRegion</a>



### -field EmfPlusRecordTypeFillPath


<a href="https://msdn.microsoft.com/29d09e61-2e44-4f2e-9356-a697b4178c71">Graphics::FillPath</a>



### -field EmfPlusRecordTypeDrawPath


<a href="https://msdn.microsoft.com/fffed788-ee5c-4c15-9480-dbedb7caa614">Graphics::DrawPath</a>



### -field EmfPlusRecordTypeFillClosedCurve


<a href="https://msdn.microsoft.com/378f0d34-7328-45e5-9f55-826bdaed3aab">FillClosedCurve Methods</a>



### -field EmfPlusRecordTypeDrawClosedCurve


<a href="https://msdn.microsoft.com/366c883b-0acf-4c2d-8ecd-18baa1c75b76">DrawClosedCurve Methods</a>



### -field EmfPlusRecordTypeDrawCurve


<a href="https://msdn.microsoft.com/3b29e150-26ac-46c6-8aa5-984aeb03392a">DrawCurve Methods</a>



### -field EmfPlusRecordTypeDrawBeziers


<a href="https://msdn.microsoft.com/af91f612-7e65-4a36-8449-32410d275b00">DrawBeziers Methods</a>



### -field EmfPlusRecordTypeDrawImage


<a href="https://msdn.microsoft.com/c9577988-e52f-4f71-ab1b-51bb5368812e">DrawImage Methods</a> (all methods that do not receive an array of destination points)


### -field EmfPlusRecordTypeDrawImagePoints


<a href="https://msdn.microsoft.com/c9577988-e52f-4f71-ab1b-51bb5368812e">DrawImage Methods</a> (all methods that receive an array of destination points)


### -field EmfPlusRecordTypeDrawString


<a href="https://msdn.microsoft.com/b3568ed9-e359-4916-a83d-7553c021d197">DrawString Methods</a>



### -field EmfPlusRecordTypeSetRenderingOrigin


<a href="https://msdn.microsoft.com/2e568966-8f37-460a-8715-76e67593001b">Graphics::SetRenderingOrigin</a>



### -field EmfPlusRecordTypeSetAntiAliasMode


<a href="https://msdn.microsoft.com/d42ae7c7-9381-4613-bb65-76683873a63a">Graphics::SetSmoothingMode</a>



### -field EmfPlusRecordTypeSetTextRenderingHint


<a href="https://msdn.microsoft.com/6ea9da15-a894-4b88-8615-bdfec19f4c1c">Graphics::SetTextRenderingHint</a>



### -field EmfPlusRecordTypeSetTextContrast


<a href="https://msdn.microsoft.com/5bd9b12f-8438-412d-a7df-5fd5d35d6187">Graphics::SetTextContrast</a>



### -field EmfPlusRecordTypeSetInterpolationMode


<a href="https://msdn.microsoft.com/1624691c-fbf0-4d14-8d48-e7c69e0100aa">Graphics::SetInterpolationMode</a>



### -field EmfPlusRecordTypeSetPixelOffsetMode


<a href="https://msdn.microsoft.com/2e93a8b1-e44d-4bd9-86bc-4291719afe9c">Graphics::SetPixelOffsetMode</a>



### -field EmfPlusRecordTypeSetCompositingMode


<a href="https://msdn.microsoft.com/93367fac-4f61-4082-9f67-13028f1b8a94">Graphics::SetCompositingMode</a>



### -field EmfPlusRecordTypeSetCompositingQuality


<a href="https://msdn.microsoft.com/e3544a81-d039-4bd6-89ea-d3883c95f7a9">Graphics::SetCompositingQuality</a>



### -field EmfPlusRecordTypeSave


<a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a>



### -field EmfPlusRecordTypeRestore


<a href="https://msdn.microsoft.com/34058862-9b3f-4ad4-bf57-904bbea50c4d">Graphics::Restore</a>



### -field EmfPlusRecordTypeBeginContainer


<a href="https://msdn.microsoft.com/4e860c19-a4db-4ebf-9e00-52c3e3f39e14">Graphics::BeginContainer</a>



### -field EmfPlusRecordTypeBeginContainerNoParams


<a href="https://msdn.microsoft.com/90d2c126-01ed-4ff3-af99-a79a88c48ce5">Graphics::BeginContainer</a>



### -field EmfPlusRecordTypeEndContainer


<a href="https://msdn.microsoft.com/431f2d85-ae7e-49e5-9240-00dd242b7390">Graphics::EndContainer</a>



### -field EmfPlusRecordTypeSetWorldTransform


<a href="https://msdn.microsoft.com/458b62ad-04f0-4202-92db-b1fcf43b3ffa">Graphics::SetTransform</a>



### -field EmfPlusRecordTypeResetWorldTransform


<a href="https://msdn.microsoft.com/10357224-cfbd-4d02-af94-93cdff80d466">Graphics::ResetTransform</a>



### -field EmfPlusRecordTypeMultiplyWorldTransform


<a href="https://msdn.microsoft.com/46f90c3e-ed70-40ba-a8e8-1b1d3276862d">Graphics::MultiplyTransform</a>



### -field EmfPlusRecordTypeTranslateWorldTransform


<a href="https://msdn.microsoft.com/99b51fb7-b1de-421f-9743-bf6a5ec758ef">Graphics::TranslateTransform</a>



### -field EmfPlusRecordTypeScaleWorldTransform


<a href="https://msdn.microsoft.com/040bfd10-1a2b-4277-9d27-0919d9efe371">Graphics::ScaleTransform</a>



### -field EmfPlusRecordTypeRotateWorldTransform


<a href="https://msdn.microsoft.com/554cd11e-9b22-48c5-a823-bd29f879fba7">Graphics::RotateTransform</a>



### -field EmfPlusRecordTypeSetPageTransform


<a href="https://msdn.microsoft.com/1efcce43-18ed-4f81-933b-ea7fcaf0226b">Graphics::SetPageScale</a> and <a href="https://msdn.microsoft.com/f931ac83-df22-426b-9323-7c0857903410">Graphics::SetPageUnit</a>



### -field EmfPlusRecordTypeResetClip


<a href="https://msdn.microsoft.com/f3fcb50c-30c3-4a57-ab99-ebe7d05ede8f">Graphics::ResetClip</a>



### -field EmfPlusRecordTypeSetClipRect


<a href="https://msdn.microsoft.com/d014787c-081c-4490-b364-dc6d5a9b6ee7">Graphics::SetClip</a> and <a href="https://msdn.microsoft.com/a39ef640-a286-4007-9cec-2b4f1f72e6db">Graphics::SetClip</a>



### -field EmfPlusRecordTypeSetClipPath


<a href="https://msdn.microsoft.com/5c266648-77b7-486e-a2e0-b70e397bea01">Graphics::SetClip</a>



### -field EmfPlusRecordTypeSetClipRegion


<a href="https://msdn.microsoft.com/0968120f-ab5d-4f04-bf55-3e6fefc52336">Graphics::SetClip</a>



### -field EmfPlusRecordTypeOffsetClip


<a href="https://msdn.microsoft.com/2ae4af90-2612-4b00-b47d-0155e98bffa5">TranslateClip Methods</a>



### -field EmfPlusRecordTypeDrawDriverString


<a href="https://msdn.microsoft.com/daed7b4e-5284-4a38-bd33-274618f01027">Graphics::DrawDriverString</a>



### -field EmfPlusRecordTypeStrokeFillPath


### -field EmfPlusRecordTypeSerializableObject


### -field EmfPlusRecordTypeSetTSGraphics


### -field EmfPlusRecordTypeSetTSClip


### -field EmfPlusRecordTotal


### -field EmfPlusRecordTypeMax


### -field EmfPlusRecordTypeMin


#### - EmfPlusRecordTypeSetGammaValue

