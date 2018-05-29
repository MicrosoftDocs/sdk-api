---
UID: TP:wibe
ms.assetid: d29980a8-57dd-3a84-8b40-97d870d7b460
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# WPF Bitmap Effects



Overview of the WPF Bitmap Effects technology.

To develop WPF Bitmap Effects, you need these headers:

 * [mileffects.h](..\mileffects\index.md)

For the programming guide, see [WPF Bitmap Effects](/previous-versions/windows/desktop/wibe).

## Structures

| Title   | Description   |
| ---- |:---- |
| [MILMatrixF structure](..\mileffects\ns-mileffects-milmatrixf.md) | Represents a 4x4 affine transformation matrix. |
| [MilMatrix3x2D structure](..\mileffects\ns-mileffects-milmatrix3x2d.md) | Represents a 3x3 matrix. |
| [MilPoint2D structure](..\mileffects\ns-mileffects-milpoint2d.md) | Represents an x- and y-coordinate pair in two-dimensional space. |
| [MilRectD structure](..\mileffects\ns-mileffects-milrectd.md) | Describes the width, height, and location of a rectangle. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IMILBitmapEffect interface](..\mileffects\nn-mileffects-imilbitmapeffect.md) | Exposes methods that define a Windows Presentation Foundation (WPF) bitmap effect. |
| [IMILBitmapEffectConnections interface](..\mileffects\nn-mileffects-imilbitmapeffectconnections.md) | Exposes methods used to retrieve input and output connectors exposed by the bitmap effect. |
| [IMILBitmapEffectConnectionsInfo interface](..\mileffects\nn-mileffects-imilbitmapeffectconnectionsinfo.md) | Exposes methods that retrieves information about what input and output pins are exposed by the bitmap effect. |
| [IMILBitmapEffectConnector interface](..\mileffects\nn-mileffects-imilbitmapeffectconnector.md) | Exposes methods that define an effect output pin. |
| [IMILBitmapEffectConnectorInfo interface](..\mileffects\nn-mileffects-imilbitmapeffectconnectorinfo.md) | Exposes methods that retrieve information about a specific input or output connector pin. |
| [IMILBitmapEffectEvents interface](..\mileffects\nn-mileffects-imilbitmapeffectevents.md) | Exposes methods that define an effect event. |
| [IMILBitmapEffectFactory interface](..\mileffects\nn-mileffects-imilbitmapeffectfactory.md) | Exposes methods used to create Windows Presentation Foundation (WPF) Microsoft Win32 bitmap effect objects. |
| [IMILBitmapEffectGroup interface](..\mileffects\nn-mileffects-imilbitmapeffectgroup.md) | Exposes methods used to access a group of effects. |
| [IMILBitmapEffectGroupImpl interface](..\mileffects\nn-mileffects-imilbitmapeffectgroupimpl.md) | Exposes methods that define an effect group. |
| [IMILBitmapEffectImpl interface](..\mileffects\nn-mileffects-imilbitmapeffectimpl.md) | Exposes methods that define an an out IMILBitmapEffect object. |
| [IMILBitmapEffectInputConnector interface](..\mileffects\nn-mileffects-imilbitmapeffectinputconnector.md) | Exposes methods that define an input connect. |
| [IMILBitmapEffectInteriorInputConnector interface](..\mileffects\nn-mileffects-imilbitmapeffectinteriorinputconnector.md) | Exposes methods that define an interior input connector. |
| [IMILBitmapEffectInteriorOutputConnector interface](..\mileffects\nn-mileffects-imilbitmapeffectinterioroutputconnector.md) | Exposes methods that define an interior output connector. |
| [IMILBitmapEffectOutputConnector interface](..\mileffects\nn-mileffects-imilbitmapeffectoutputconnector.md) | Exposes methods that define an output connector. |
| [IMILBitmapEffectOutputConnectorImpl interface](..\mileffects\nn-mileffects-imilbitmapeffectoutputconnectorimpl.md) | Exposes methods that define an output connector. |
| [IMILBitmapEffectPrimitive interface](..\mileffects\nn-mileffects-imilbitmapeffectprimitive.md) | Exposes methods that create a bitmap effect's output. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects. |
| [IMILBitmapEffectPrimitiveImpl interface](..\mileffects\nn-mileffects-imilbitmapeffectprimitiveimpl.md) | Exposes methods that report the state of a bitmap effect. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects. |
| [IMILBitmapEffectRenderContext interface](..\mileffects\nn-mileffects-imilbitmapeffectrendercontext.md) | Exposes methods that define a IMILBitmapEffectRenderContext object. |
| [IMILBitmapEffectRenderContextImpl interface](..\mileffects\nn-mileffects-imilbitmapeffectrendercontextimpl.md) | Exposes methods that define a IMILBitmapEffectRenderContext. |
| [IMILBitmapEffects interface](..\mileffects\nn-mileffects-imilbitmapeffects.md) | Exposes methods that define an enumeration of effects. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IMILBitmapEffect::GetOutput](..\mileffects\nf-mileffects-imilbitmapeffect-getoutput.md) | Gets the output of the effect. |
| [IMILBitmapEffect::GetParentEffect](..\mileffects\nf-mileffects-imilbitmapeffect-getparenteffect.md) | Gets a parent of the effect. |
| [IMILBitmapEffect::SetInputSource](..\mileffects\nf-mileffects-imilbitmapeffect-setinputsource.md) | Sets the effect input source. |
| [IMILBitmapEffectConnections::GetInputConnector](..\mileffects\nf-mileffects-imilbitmapeffectconnections-getinputconnector.md) | Retrieves the input connector associated with the given pin index. |
| [IMILBitmapEffectConnections::GetOutputConnector](..\mileffects\nf-mileffects-imilbitmapeffectconnections-getoutputconnector.md) | Retrieves the output connector associated with the given pin index. |
| [IMILBitmapEffectConnectionsInfo::GetInputConnectorInfo](..\mileffects\nf-mileffects-imilbitmapeffectconnectionsinfo-getinputconnectorinfo.md) | Retrieves the IMILBitmapEffectConnectorInfo associated with the given input pin. |
| [IMILBitmapEffectConnectionsInfo::GetNumberInputs](..\mileffects\nf-mileffects-imilbitmapeffectconnectionsinfo-getnumberinputs.md) | Retrieves the number of input pins the bitmap effect implements. |
| [IMILBitmapEffectConnectionsInfo::GetNumberOutputs](..\mileffects\nf-mileffects-imilbitmapeffectconnectionsinfo-getnumberoutputs.md) | Retrieves the number of output pins the bitmap effect implements. |
| [IMILBitmapEffectConnectionsInfo::GetOutputConnectorInfo](..\mileffects\nf-mileffects-imilbitmapeffectconnectionsinfo-getoutputconnectorinfo.md) | Retrieves the IMILBitmapEffectConnectorInfo associated with the given output pin. |
| [IMILBitmapEffectConnector::GetBitmapEffect](..\mileffects\nf-mileffects-imilbitmapeffectconnector-getbitmapeffect.md) | Gets the IMILBitmapEffect associated with the connector. |
| [IMILBitmapEffectConnector::IsConnected](..\mileffects\nf-mileffects-imilbitmapeffectconnector-isconnected.md) | Determines whether the connector is connected to an effect. |
| [IMILBitmapEffectConnectorInfo::GetFormat](..\mileffects\nf-mileffects-imilbitmapeffectconnectorinfo-getformat.md) | Retrieves the pixel format for the given pin. |
| [IMILBitmapEffectConnectorInfo::GetIndex](..\mileffects\nf-mileffects-imilbitmapeffectconnectorinfo-getindex.md) | Retrieves the zero based index value for the pin. |
| [IMILBitmapEffectConnectorInfo::GetNumberFormats](..\mileffects\nf-mileffects-imilbitmapeffectconnectorinfo-getnumberformats.md) | Retrieves the number of pixel formats supported by the pin. |
| [IMILBitmapEffectConnectorInfo::GetOptimalFormat](..\mileffects\nf-mileffects-imilbitmapeffectconnectorinfo-getoptimalformat.md) | Retrieves the optimal pixel format for the pin. |
| [IMILBitmapEffectEvents::DirtyRegion](..\mileffects\nf-mileffects-imilbitmapeffectevents-dirtyregion.md) | Invalidates the specified region of the given IMILBitmapEffectPrimitive. |
| [IMILBitmapEffectEvents::PropertyChange](..\mileffects\nf-mileffects-imilbitmapeffectevents-propertychange.md) | Notifies an IMILBitmapEffectPrimitive of a property change. |
| [IMILBitmapEffectFactory::CreateContext](..\mileffects\nf-mileffects-imilbitmapeffectfactory-createcontext.md) | Creates an IMILBitmapEffectRenderContext object. |
| [IMILBitmapEffectFactory::CreateEffectOuter](..\mileffects\nf-mileffects-imilbitmapeffectfactory-createeffectouter.md) | Creates an outer IMILBitmapEffect object. |
| [IMILBitmapEffectFactory::CreateEffect](..\mileffects\nf-mileffects-imilbitmapeffectfactory-createeffect.md) | Creates an IMILBitmapEffect object. |
| [IMILBitmapEffectGroup::Add](..\mileffects\nf-mileffects-imilbitmapeffectgroup-add.md) | Adds an effect to the IMILBitmapEffectGroup. |
| [IMILBitmapEffectGroup::GetInteriorInputConnector](..\mileffects\nf-mileffects-imilbitmapeffectgroup-getinteriorinputconnector.md) | Retrieves the input connector for an effect at the given index. |
| [IMILBitmapEffectGroup::GetInteriorOutputConnector](..\mileffects\nf-mileffects-imilbitmapeffectgroup-getinterioroutputconnector.md) | Retrieves the output connector for an effect at the given index. |
| [IMILBitmapEffectGroupImpl::GetChildren](..\mileffects\nf-mileffects-imilbitmapeffectgroupimpl-getchildren.md) | Gets the children of the effect group. |
| [IMILBitmapEffectGroupImpl::GetNumberChildren](..\mileffects\nf-mileffects-imilbitmapeffectgroupimpl-getnumberchildren.md) | Retrieves the number of children in an effect group. |
| [IMILBitmapEffectGroupImpl::Preprocess](..\mileffects\nf-mileffects-imilbitmapeffectgroupimpl-preprocess.md) | Pre-process the given render context. |
| [IMILBitmapEffectImpl::GetInputBitmapSource](..\mileffects\nf-mileffects-imilbitmapeffectimpl-getinputbitmapsource.md) | Gets the input bitmap source of the effect of the given render context. |
| [IMILBitmapEffectImpl::GetInputSourceBounds](..\mileffects\nf-mileffects-imilbitmapeffectimpl-getinputsourcebounds.md) | Gets the bounds of the input source. |
| [IMILBitmapEffectImpl::GetInputSource](..\mileffects\nf-mileffects-imilbitmapeffectimpl-getinputsource.md) | Retrieves the input IWICBitmapSource Interface. |
| [IMILBitmapEffectImpl::GetOutputBitmapSource](..\mileffects\nf-mileffects-imilbitmapeffectimpl-getoutputbitmapsource.md) | Gets the output bitmap source of the effect of the given render context. |
| [IMILBitmapEffectImpl::Initialize](..\mileffects\nf-mileffects-imilbitmapeffectimpl-initialize.md) | Initializes the effect with the given object. |
| [IMILBitmapEffectImpl::IsInPlaceModificationAllowed](..\mileffects\nf-mileffects-imilbitmapeffectimpl-isinplacemodificationallowed.md) | Determines whether the effect allows in-place modifications. |
| [IMILBitmapEffectImpl::SetParentEffect](..\mileffects\nf-mileffects-imilbitmapeffectimpl-setparenteffect.md) | Sets the parent of the effect. |
| [IMILBitmapEffectInputConnector::ConnectTo](..\mileffects\nf-mileffects-imilbitmapeffectinputconnector-connectto.md) | Connects the input connector to the given output connector. |
| [IMILBitmapEffectInputConnector::GetConnection](..\mileffects\nf-mileffects-imilbitmapeffectinputconnector-getconnection.md) | Gets the IMILBitmapEffectOutputConnector the input connector is connected to. |
| [IMILBitmapEffectInteriorInputConnector::GetInputConnector](..\mileffects\nf-mileffects-imilbitmapeffectinteriorinputconnector-getinputconnector.md) | Gets the IMILBitmapEffectInputConnector associated with the interior connector. |
| [IMILBitmapEffectInteriorOutputConnector::GetOutputConnector](..\mileffects\nf-mileffects-imilbitmapeffectinterioroutputconnector-getoutputconnector.md) | Gets the IMILBitmapEffectOutputConnector associated with the interior output connector. |
| [IMILBitmapEffectOutputConnector::GetConnection](..\mileffects\nf-mileffects-imilbitmapeffectoutputconnector-getconnection.md) | Gets the IMILBitmapEffectInputConnector associated with the output connector. |
| [IMILBitmapEffectOutputConnector::GetNumberConnections](..\mileffects\nf-mileffects-imilbitmapeffectoutputconnector-getnumberconnections.md) | Retrieves the number of connections the output connector has. |
| [IMILBitmapEffectOutputConnectorImpl::AddBackLink](..\mileffects\nf-mileffects-imilbitmapeffectoutputconnectorimpl-addbacklink.md) | IMILBitmapEffectOutputConnectorImpl |
| [IMILBitmapEffectOutputConnectorImpl::RemoveBackLink](..\mileffects\nf-mileffects-imilbitmapeffectoutputconnectorimpl-removebacklink.md) | IMILBitmapEffectOutputConnectorImpl |
| [IMILBitmapEffectPrimitive::GetAffineMatrix](..\mileffects\nf-mileffects-imilbitmapeffectprimitive-getaffinematrix.md) | Retrieves the affine transormation matrix for the effect. |
| [IMILBitmapEffectPrimitive::GetOutput](..\mileffects\nf-mileffects-imilbitmapeffectprimitive-getoutput.md) | Performs pixel processing for the bitmap effect. |
| [IMILBitmapEffectPrimitive::HasAffineTransform](..\mileffects\nf-mileffects-imilbitmapeffectprimitive-hasaffinetransform.md) | Determines whether the effect has an affine transform. |
| [IMILBitmapEffectPrimitive::HasInverseTransform](..\mileffects\nf-mileffects-imilbitmapeffectprimitive-hasinversetransform.md) | Determines whether the effect has an inverse transform. |
| [IMILBitmapEffectPrimitive::TransformPoint](..\mileffects\nf-mileffects-imilbitmapeffectprimitive-transformpoint.md) | Transforms the given point. |
| [IMILBitmapEffectPrimitive::TransformRect](..\mileffects\nf-mileffects-imilbitmapeffectprimitive-transformrect.md) | Transforms the output of the given rectangle. |
| [IMILBitmapEffectPrimitiveImpl::IsDirty](..\mileffects\nf-mileffects-imilbitmapeffectprimitiveimpl-isdirty.md) | Determines whether the effect needs to be updated. |
| [IMILBitmapEffectPrimitiveImpl::IsVolatile](..\mileffects\nf-mileffects-imilbitmapeffectprimitiveimpl-isvolatile.md) | Determines whether the current effect is considered volatile. If an effect is volatile, the effects framework will not attempt to cache the effect's output. |
| [IMILBitmapEffectRenderContext::GetFinalTransform](..\mileffects\nf-mileffects-imilbitmapeffectrendercontext-getfinaltransform.md) | Gets the final MILMatrixF transform. |
| [IMILBitmapEffectRenderContext::GetOutputDPI](..\mileffects\nf-mileffects-imilbitmapeffectrendercontext-getoutputdpi.md) | Gets the output dots per inch (dpi). |
| [IMILBitmapEffectRenderContext::GetOutputPixelFormat](..\mileffects\nf-mileffects-imilbitmapeffectrendercontext-getoutputpixelformat.md) | Gets the output pixel format GUID. |
| [IMILBitmapEffectRenderContext::SetInitialTransform](..\mileffects\nf-mileffects-imilbitmapeffectrendercontext-setinitialtransform.md) | Gets the initial MILMatrixF transform. |
| [IMILBitmapEffectRenderContext::SetOutputDPI](..\mileffects\nf-mileffects-imilbitmapeffectrendercontext-setoutputdpi.md) | Sets the output dots per inch (dpi). |
| [IMILBitmapEffectRenderContext::SetOutputPixelFormat](..\mileffects\nf-mileffects-imilbitmapeffectrendercontext-setoutputpixelformat.md) | Sets the output pixel format. |
| [IMILBitmapEffectRenderContext::SetRegionOfInterest](..\mileffects\nf-mileffects-imilbitmapeffectrendercontext-setregionofinterest.md) | Sets the region of interest for the effect. |
| [IMILBitmapEffectRenderContext::SetUseSoftwareRenderer](..\mileffects\nf-mileffects-imilbitmapeffectrendercontext-setusesoftwarerenderer.md) | Sets a value to indicate whether to use software rendering. |
| [IMILBitmapEffectRenderContextImpl::GetOutputBounds](..\mileffects\nf-mileffects-imilbitmapeffectrendercontextimpl-getoutputbounds.md) | Gets the output bounds of the render context. |
| [IMILBitmapEffectRenderContextImpl::GetTransform](..\mileffects\nf-mileffects-imilbitmapeffectrendercontextimpl-gettransform.md) | Gets the matrix transform of the render context. |
| [IMILBitmapEffectRenderContextImpl::GetUseSoftwareRenderer](..\mileffects\nf-mileffects-imilbitmapeffectrendercontextimpl-getusesoftwarerenderer.md) | Gets a value that indicates whether to use software rendering. |
| [IMILBitmapEffectRenderContextImpl::UpdateOutputBounds](..\mileffects\nf-mileffects-imilbitmapeffectrendercontextimpl-updateoutputbounds.md) | Updates the output bounds with the given region. |
| [IMILBitmapEffectRenderContextImpl::UpdateTransform](..\mileffects\nf-mileffects-imilbitmapeffectrendercontextimpl-updatetransform.md) | Updates the output transform with the new matrix. |
| [IMILBitmapEffects::Item](..\mileffects\nf-mileffects-imilbitmapeffects-item.md) | Retrieves the effect at the given index. |
| [IMILBitmapEffects::_NewEnum](..\mileffects\nf-mileffects-imilbitmapeffects-_newenum.md) | Retrieves a new enumeration. |
