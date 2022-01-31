---
UID: NE:wingdi.__unnamed_enum_2
title: DISPLAYCONFIG_SCALING (wingdi.h)
description: The DISPLAYCONFIG_SCALING enumeration specifies the scaling transformation applied to content displayed on a video present network (VidPN) present path.
helpviewer_keywords: ["CCD_Enumerations_67f71fcc-f83c-4a11-94d4-169ab6d55f7c.xml","DISPLAYCONFIG_SCALING","DISPLAYCONFIG_SCALING enumeration [Display Devices]","DISPLAYCONFIG_SCALING_ASPECTRATIOCENTEREDMAX","DISPLAYCONFIG_SCALING_CENTERED","DISPLAYCONFIG_SCALING_CUSTOM","DISPLAYCONFIG_SCALING_FORCE_UINT32","DISPLAYCONFIG_SCALING_IDENTITY","DISPLAYCONFIG_SCALING_PREFERRED","DISPLAYCONFIG_SCALING_STRETCHED","display.displayconfig_scaling","wingdi/DISPLAYCONFIG_SCALING","wingdi/DISPLAYCONFIG_SCALING_ASPECTRATIOCENTEREDMAX","wingdi/DISPLAYCONFIG_SCALING_CENTERED","wingdi/DISPLAYCONFIG_SCALING_CUSTOM","wingdi/DISPLAYCONFIG_SCALING_FORCE_UINT32","wingdi/DISPLAYCONFIG_SCALING_IDENTITY","wingdi/DISPLAYCONFIG_SCALING_PREFERRED","wingdi/DISPLAYCONFIG_SCALING_STRETCHED"]
old-location: display\displayconfig_scaling.htm
tech.root: display
ms.assetid: 6f073aa6-2647-4a51-9256-b2da488fd382
ms.date: 12/05/2018
ms.keywords: CCD_Enumerations_67f71fcc-f83c-4a11-94d4-169ab6d55f7c.xml, DISPLAYCONFIG_SCALING, DISPLAYCONFIG_SCALING enumeration [Display Devices], DISPLAYCONFIG_SCALING_ASPECTRATIOCENTEREDMAX, DISPLAYCONFIG_SCALING_CENTERED, DISPLAYCONFIG_SCALING_CUSTOM, DISPLAYCONFIG_SCALING_FORCE_UINT32, DISPLAYCONFIG_SCALING_IDENTITY, DISPLAYCONFIG_SCALING_PREFERRED, DISPLAYCONFIG_SCALING_STRETCHED, display.displayconfig_scaling, wingdi/DISPLAYCONFIG_SCALING, wingdi/DISPLAYCONFIG_SCALING_ASPECTRATIOCENTEREDMAX, wingdi/DISPLAYCONFIG_SCALING_CENTERED, wingdi/DISPLAYCONFIG_SCALING_CUSTOM, wingdi/DISPLAYCONFIG_SCALING_FORCE_UINT32, wingdi/DISPLAYCONFIG_SCALING_IDENTITY, wingdi/DISPLAYCONFIG_SCALING_PREFERRED, wingdi/DISPLAYCONFIG_SCALING_STRETCHED
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DISPLAYCONFIG_SCALING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_SCALING
 - wingdi/DISPLAYCONFIG_SCALING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_SCALING
---

# DISPLAYCONFIG_SCALING enumeration


## -description

The DISPLAYCONFIG_SCALING enumeration specifies the scaling transformation applied to content displayed on a video present network (VidPN) present path.

## -enum-fields

### -field DISPLAYCONFIG_SCALING_IDENTITY:1

Indicates the identity transformation; the source content is presented with no change. This transformation is available only if the path's source mode has the same spatial resolution as the path's target mode.

### -field DISPLAYCONFIG_SCALING_CENTERED:2

Indicates the centering transformation; the source content is presented unscaled, centered with respect to the spatial resolution of the target mode.

### -field DISPLAYCONFIG_SCALING_STRETCHED:3

Indicates the content is scaled to fit the path's target.

### -field DISPLAYCONFIG_SCALING_ASPECTRATIOCENTEREDMAX:4

Indicates the aspect-ratio centering transformation.

### -field DISPLAYCONFIG_SCALING_CUSTOM:5

Indicates that the caller requests a custom scaling that the caller cannot describe with any of the other DISPLAYCONFIG_SCALING_XXX values. Only a hardware vendor's value-add application should use DISPLAYCONFIG_SCALING_CUSTOM, because the value-add application might require a private interface to the driver. The application can then use DISPLAYCONFIG_SCALING_CUSTOM to indicate additional context for the driver for the custom value on the specified path.

### -field DISPLAYCONFIG_SCALING_PREFERRED:128

Indicates that the caller does not have any preference for the scaling. The <a href="/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a> function will use the scaling value that was last saved in the database for the path. If such a scaling value does not exist, <b>SetDisplayConfig</b> will use the default scaling for the computer. For example, stretched (DISPLAYCONFIG_SCALING_STRETCHED) for tablet computers and aspect-ratio centered (DISPLAYCONFIG_SCALING_ASPECTRATIOCENTEREDMAX) for non-tablet computers.

### -field DISPLAYCONFIG_SCALING_FORCE_UINT32:0xFFFFFFFF

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.

## -remarks

For more information about scaling, see <a href="/windows-hardware/drivers/display/scaling-the-desktop-image">Scaling the Desktop Image</a>.
