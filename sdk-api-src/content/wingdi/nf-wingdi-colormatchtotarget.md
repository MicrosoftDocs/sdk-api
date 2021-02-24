---
UID: NF:wingdi.ColorMatchToTarget
title: ColorMatchToTarget function (wingdi.h)
description: The ColorMatchToTarget function enables you to preview colors as they would appear on the target device.
helpviewer_keywords: ["CS_DELETE_TRANSFORM","CS_DISABLE","CS_ENABLE","ColorMatchToTarget","ColorMatchToTarget function [Windows Color System]","_color_ColorMatchToTarget","wcs.colormatchtotarget","wingdi/ColorMatchToTarget"]
old-location: wcs\colormatchtotarget.htm
tech.root: WCS
ms.assetid: eb922411-0808-4404-bdaf-bf29d0cad379
ms.date: 12/05/2018
ms.keywords: CS_DELETE_TRANSFORM, CS_DISABLE, CS_ENABLE, ColorMatchToTarget, ColorMatchToTarget function [Windows Color System], _color_ColorMatchToTarget, wcs.colormatchtotarget, wingdi/ColorMatchToTarget
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ColorMatchToTarget
 - wingdi/ColorMatchToTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - ColorMatchToTarget
---

# ColorMatchToTarget function


## -description

The <b>ColorMatchToTarget</b> function enables you to preview colors as they would appear on the target device.

## -parameters

### -param hdc

Specifies the device context for previewing, generally the screen.

### -param hdcTarget

Specifies the target device context, generally a printer.

### -param action

A constant that can have one of the following values.<div> </div>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CS_ENABLE"></a><a id="cs_enable"></a><dl>
<dt><b>CS_ENABLE</b></dt>
</dl>
</td>
<td width="60%">
Map the colors to the target device's color gamut. This enables color proofing. All subsequent draw commands to the DC will render colors as they would appear on the target device.

</td>
</tr>
<tr>
<td width="40%"><a id="CS_DISABLE"></a><a id="cs_disable"></a><dl>
<dt><b>CS_DISABLE</b></dt>
</dl>
</td>
<td width="60%">
Disable color proofing.

</td>
</tr>
<tr>
<td width="40%"><a id="CS_DELETE_TRANSFORM"></a><a id="cs_delete_transform"></a><dl>
<dt><b>CS_DELETE_TRANSFORM</b></dt>
</dl>
</td>
<td width="60%">
If color management is enabled for the target profile, disable it and delete the concatenated transform.

</td>
</tr>
</table>

## -returns

If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.

## -remarks

<b>ColorMatchToTarget</b> can be used to proof the colors of a color output device on another color output device. Setting the <i>uiAction</i> parameter to CS_ENABLE causes all subsequent drawing commands to the DC to render colors as they would appear on the target device. If <i>uiAction</i> is set to CS_DISABLE, proofing is turned off. However, the current color transform is not deleted from the DC. It is just inactive.

When <b>ColorMatchToTarget</b> is called, the color transform for the target device is performed first, and then the transform to the preview device is applied to the results of the first transform. This is used primarily for checking gamut mapping conditions. Before using this function, you must enable WCS for both device contexts.

This function cannot be cascaded. While color mapping to the target is enabled by setting <i>uiAction</i> to CS_ENABLE, application changes to the color space or gamut mapping method are ignored. Those changes then take effect when color mapping to the target is disabled.

<div class="alert"><b>Note</b>  A memory leak will not occur if an application does not delete a transform using CS_DELETE_TRANSFORM. The transform will be deleted when either the device context (DC) is closed, or when the application color space is deleted. However if the transform is not going to be used again, or if the application will not be performing any more color matching on the DC, it should explicitly delete the transform to free the memory it occupies.</div>
<div> </div>
The <i>uiAction</i> parameter should only be set to CS_DELETE_TRANSFORM if color management is enabled before the <b>ColorMatchToTarget</b> function is called.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
