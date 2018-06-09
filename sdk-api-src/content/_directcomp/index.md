---
UID: TP:directcomp
ms.assetid: efb19c94-b4cc-3005-83ee-8d631642e8f9
ms.author: windowssdkdev
ms.date: 06/09/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# DirectComposition

## -description

Overview of the DirectComposition technology.

To develop DirectComposition, you need these headers:

 * [dcomp.h](../dcomp/index.md)
 * [dcompanimation.h](../dcompanimation/index.md)
 * [dcomptypes.h](../dcomptypes/index.md)

For the programming guide, see [DirectComposition](/windows/desktop/directcomp).

## Functions

| Title   | Description   |
| ---- |:---- |
| [DCompositionAttachMouseDragToHwnd function](..\dcomp\nf-dcomp-dcompositionattachmousedragtohwnd.md) | Creates an Interaction/InputSink to route mouse button down and any subsequent move and up events to the given HWND. |
| [DCompositionAttachMouseWheelToHwnd function](..\dcomp\nf-dcomp-dcompositionattachmousewheeltohwnd.md) | Creates an Interaction/InputSink to route mouse wheel messages to the given HWND. |
| [DCompositionCreateDevice function](..\dcomp\nf-dcomp-dcompositioncreatedevice.md) | Creates a new device object that can be used to create other Microsoft DirectComposition objects. |
| [DCompositionCreateDevice2 function](..\dcomp\nf-dcomp-dcompositioncreatedevice2.md) | Creates a new device object that can be used to create other Microsoft DirectComposition objects. |
| [DCompositionCreateDevice3 function](..\dcomp\nf-dcomp-dcompositioncreatedevice3.md) | Creates a new DirectComposition device object, which can be used to create other DirectComposition objects. |
| [DCompositionCreateSurfaceHandle function](..\dcomp\nf-dcomp-dcompositioncreatesurfacehandle.md) | Creates a new composition surface object that can be bound to a Microsoft DirectX swap chain or swap buffer and associated with a visual. |
| [SetAlphaSlope function](..\dcomp\nf-dcomp-setalphaslope.md) | Sets the slope of the linear function for the alpha channel. |
| [SetAlphaTableValue function](..\dcomp\nf-dcomp-setalphatablevalue.md) | Sets a value in the alpha table. |
| [SetAlphaYIntercept function](..\dcomp\nf-dcomp-setalphayintercept.md) | Sets the Y-intercept of the linear function for the alpha channel. |
| [SetAngle function](..\dcomp\nf-dcomp-setangle.md) | Sets the angle to rotate the hue. |
| [SetAngleX function](..\dcomp\nf-dcomp-setanglex.md) | Changes or animates the value of the AngleX property of a 2D skew transform. The AngleX property specifies the rotation angle, in degrees. The default value is zero. |
| [SetAngleY function](..\dcomp\nf-dcomp-setangley.md) | Changes or animates the value of the AngleY property of a 2D skew transform. The AngleY property specifies the rotation angle, in degrees. The default value is zero. |
| [SetAxisX function](..\dcomp\nf-dcomp-setaxisx.md) | Changes or animates the value of the AxisX property of a 3D rotation transform. The AxisX property specifies the x-coordinate for the axis vector of rotation. The default value is zero. |
| [SetAxisY function](..\dcomp\nf-dcomp-setaxisy.md) | Changes or animates the value of the AxisY property of a rotation transform. The AxisY property specifies the y-coordinate for the axis vector of rotation. The default value is zero. |
| [SetAxisZ function](..\dcomp\nf-dcomp-setaxisz.md) | Changes or animates the value of the AxisZ property of a 3D rotation transform. The AxisZ property specifies the z-coordinate for the axis vector of rotation. The default value is 1.0. |
| [SetBlackPointX function](..\dcomp\nf-dcomp-setblackpointx.md) | Sets the x value of the black point. |
| [SetBlackPointY function](..\dcomp\nf-dcomp-setblackpointy.md) | Sets the y value of the black point. |
| [SetBlue function](..\dcomp\nf-dcomp-setblue.md) | Sets the blue value for the color of the shadow. |
| [SetBlueSlope function](..\dcomp\nf-dcomp-setblueslope.md) | The slope of the linear function for the blue channel. |
| [SetBlueTableValue function](..\dcomp\nf-dcomp-setbluetablevalue.md) | Sets a value in the blue table. |
| [SetBlueYIntercept function](..\dcomp\nf-dcomp-setblueyintercept.md) | Sets the Y-intercept of the linear function for the blue channel. |
| [SetBottom function](..\dcomp\nf-dcomp-setbottom.md) | Animates or changes the value of the Bottom property of a clip rectangle. |
| [SetBottomLeftRadiusX function](..\dcomp\nf-dcomp-setbottomleftradiusx.md) | Changes or animates the value of the BottomLeftRadiusX property of this clip. The BottomLeftRadiusX property specifies the x radius of the ellipse that rounds the lower-left corner of the clip. |
| [SetBottomLeftRadiusY function](..\dcomp\nf-dcomp-setbottomleftradiusy.md) | Changes or animates the value of the BottomLeftRadiusY property of this clip. The BottomLeftRadiusY property specifies the y radius of the ellipse that rounds the lower-left corner of the clip. |
| [SetBottomRightRadiusX function](..\dcomp\nf-dcomp-setbottomrightradiusx.md) | Changes or animates the value of the BottomRightRadiusX property of this clip. The BottomRightRadiusX property specifies the x radius of the ellipse that rounds the lower-right corner of the clip. |
| [SetBottomRightRadiusY function](..\dcomp\nf-dcomp-setbottomrightradiusy.md) | Changes or animates the value of the BottomRightRadiusY property of this clip. The BottomRightRadiusY property specifies the y radius of the ellipse that rounds the lower-right corner of the clip. |
| [SetCenterX function](..\dcomp\nf-dcomp-setcenterx.md) | Changes or animates the value of the CenterX property of a 3D rotation transform. The CenterX property specifies the x-coordinate of the point about which the rotation is performed. The default value is zero. |
| [SetCenterY function](..\dcomp\nf-dcomp-setcentery.md) | Changes or animates the value of the CenterY property of a 3D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed. The default value is zero. |
| [SetCenterZ function](..\dcomp\nf-dcomp-setcenterz.md) | Changes or animates the value of the CenterZ property of a 3D rotation transform. The CenterZ property specifies the z-coordinate of the point about which the rotation is performed. The default value is zero. |
| [SetClip function](..\dcomp\nf-dcomp-setclip.md) | Sets the Clip property of this visual to the specified rectangular region or clip object. |
| [SetCoefficient1 function](..\dcomp\nf-dcomp-setcoefficient1.md) | Sets the first coefficient for the equation used to composite the two input images. |
| [SetCoefficient2 function](..\dcomp\nf-dcomp-setcoefficient2.md) | Sets the second coefficient for the equation used to composite the two input images. |
| [SetCoefficient3 function](..\dcomp\nf-dcomp-setcoefficient3.md) | Sets the third coefficient for the equation used to composite the two input images. |
| [SetCoefficient4 function](..\dcomp\nf-dcomp-setcoefficient4.md) | Sets the fourth coefficient for the equation used to composite the two input images. |
| [SetGreenSlope function](..\dcomp\nf-dcomp-setgreenslope.md) | Sets the slope of the linear function for the green channel. |
| [SetGreenTableValue function](..\dcomp\nf-dcomp-setgreentablevalue.md) | Sets a value in the green table. |
| [SetGreenYIntercept function](..\dcomp\nf-dcomp-setgreenyintercept.md) | Sets the Y-intercept of the linear function for the green channel. |
| [SetLeft function](..\dcomp\nf-dcomp-setleft.md) | Animates or changes the value of the Left property of a clip rectangle. |
| [SetMatrixElement function](..\dcomp\nf-dcomp-setmatrixelement.md) | Sets an element of the color matrix. |
| [SetOffsetX function](..\dcomp\nf-dcomp-setoffsetx.md) | Changes or animates the value of the OffsetX property of a 3D translation transform effect. |
| [SetOffsetY function](..\dcomp\nf-dcomp-setoffsety.md) | Changes or animates the value of the OffsetY property of a 3D translation transform effect. |
| [SetOffsetZ function](..\dcomp\nf-dcomp-setoffsetz.md) | Changes or animates the value of the OffsetZ property of a 3D translation transform effect. |
| [SetOpacity function](..\dcomp\nf-dcomp-setopacity.md) | Animates or changes the value of the Opacity property. |
| [SetRed function](..\dcomp\nf-dcomp-setred.md) | Sets the red value for the color of the shadow. |
| [SetRedSlope function](..\dcomp\nf-dcomp-setredslope.md) | Sets the slope of the linear function for the red channel. |
| [SetRedTableValue function](..\dcomp\nf-dcomp-setredtablevalue.md) | Sets a value in the red table. |
| [SetRedYIntercept function](..\dcomp\nf-dcomp-setredyintercept.md) | Sets the Y-intercept of the linear function for the red channel. |
| [SetRight function](..\dcomp\nf-dcomp-setright.md) | Animates or changes the value of the Right property of a clip rectangle. |
| [SetScaleX function](..\dcomp\nf-dcomp-setscalex.md) | Changes or animates the value of the ScaleX property of a 3D scale transform. |
| [SetScaleY function](..\dcomp\nf-dcomp-setscaley.md) | Changes or animates the value of the ScaleY property of a scale transform. |
| [SetScaleZ function](..\dcomp\nf-dcomp-setscalez.md) | Changes or animates the value of the ScaleZ property of a scale transform. |
| [SetStandardDeviation function](..\dcomp\nf-dcomp-setstandarddeviation.md) | Sets the amount of blur to be applied to the image. |
| [SetTop function](..\dcomp\nf-dcomp-settop.md) | Animates or changes the value of the Top property of a clip rectangle. |
| [SetTopLeftRadiusX function](..\dcomp\nf-dcomp-settopleftradiusx.md) | Changes or animates the value of the TopLeftRadiusX property of this clip. The TopLeftRadiusX property specifies the x radius of the ellipse that rounds the top-left corner of the clip. |
| [SetTopLeftRadiusY function](..\dcomp\nf-dcomp-settopleftradiusy.md) | Changes or animates the value of the TopLeftRadiusY property of this clip. The TopLeftRadiusY property specifies the y radius of the ellipse that rounds the top-left corner of the clip. |
| [SetTopRightRadiusX function](..\dcomp\nf-dcomp-settoprightradiusx.md) | Changes or animates the value of the TopRightRadiusX property of this clip. The TopRightRadiusX property specifies the x radius of the ellipse that rounds the top-right corner of the clip. |
| [SetTopRightRadiusY function](..\dcomp\nf-dcomp-settoprightradiusy.md) | Changes or animates the value of the TopRightRadiusY property of this clip. The TopRightRadiusY property specifies the y radius of the ellipse that rounds the top-right corner of the clip. |
| [SetTransform function](..\dcomp\nf-dcomp-settransform.md) | Sets the Transform property of this visual. The Transform property specifies a 3D transform used to modify the coordinate system of this visual. The property can specify either a 4-by-4 transform matrix or a transform object. |
| [SetTransformMatrixElement function](..\dcomp\nf-dcomp-settransformmatrixelement.md) | Sets an element of the transform matrix of the effect. |
| [SetWhitePointX function](..\dcomp\nf-dcomp-setwhitepointx.md) | Sets the x value of the white point. |
| [SetWhitePointY function](..\dcomp\nf-dcomp-setwhitepointy.md) | Sets the y value of the white point. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [DCOMPOSITION_FRAME_STATISTICS structure](..\dcomptypes\ns-dcomptypes-dcomposition_frame_statistics.md) | Describes timing and composition statistics for a frame. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [DCOMPOSITION_BACKFACE_VISIBILITY enumeration](..\dcomptypes\ne-dcomptypes-dcomposition_backface_visibility.md) | Specifies the backface visibility to be applied to a visual. |
| [DCOMPOSITION_BITMAP_INTERPOLATION_MODE enumeration](..\dcomptypes\ne-dcomptypes-dcomposition_bitmap_interpolation_mode.md) | Specifies the interpolation mode to be used when a bitmap is composed with any transform where the pixels in the bitmap don't line up exactly one-to-one with pixels on screen. |
| [DCOMPOSITION_BORDER_MODE enumeration](..\dcomptypes\ne-dcomptypes-dcomposition_border_mode.md) | Specifies the border mode to use when composing a bitmap or applying a clip with any transform such that the edges of the bitmap or clip are not axis-aligned with integer coordinates. |
| [DCOMPOSITION_COMPOSITE_MODE enumeration](..\dcomptypes\ne-dcomptypes-dcomposition_composite_mode.md) | The mode to use to blend the bitmap content of a visual with the render target. |
| [DCOMPOSITION_OPACITY_MODE enumeration](..\dcomptypes\ne-dcomptypes-dcomposition_opacity_mode.md) | Specifies how the effective opacity value of a visual is applied to that visual’s content and children. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IDCompositionAnimation interface](..\dcompanimation\nn-dcompanimation-idcompositionanimation.md) | Represents a function for animating one or more properties of one or more Microsoft DirectComposition objects. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDCompositionAnimation::AddCubic](..\dcompanimation\nf-dcompanimation-idcompositionanimation-addcubic.md) | Adds a cubic polynomial segment to the animation function. |
| [IDCompositionAnimation::AddRepeat](..\dcompanimation\nf-dcompanimation-idcompositionanimation-addrepeat.md) | Adds a repeat segment that causes the specified portion of an animation function to be repeated. |
| [IDCompositionAnimation::AddSinusoidal](..\dcompanimation\nf-dcompanimation-idcompositionanimation-addsinusoidal.md) | Adds a sinusoidal segment to the animation function. |
| [IDCompositionAnimation::End](..\dcompanimation\nf-dcompanimation-idcompositionanimation-end.md) | Adds an end segment that marks the end of an animation function. |
| [IDCompositionAnimation::Reset](..\dcompanimation\nf-dcompanimation-idcompositionanimation-reset.md) | Resets the animation function so that it contains no segments. |
| [IDCompositionAnimation::SetAbsoluteBeginTime](..\dcompanimation\nf-dcompanimation-idcompositionanimation-setabsolutebegintime.md) | Sets the absolute time at which the animation function starts. |
