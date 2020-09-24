---
UID: NS:ddrawint._DD_MISCELLANEOUS2CALLBACKS
title: DD_MISCELLANEOUS2CALLBACKS (ddrawint.h)
description: The DD_MISCELLANEOUS2CALLBACKS structure is used to return the addresses of miscellaneous callback routines.
helpviewer_keywords: ["*PDD_MISCELLANEOUS2CALLBACKS","DD_MISCELLANEOUS2CALLBACKS","DD_MISCELLANEOUS2CALLBACKS structure [Display Devices]","PDD_MISCELLANEOUS2CALLBACKS","PDD_MISCELLANEOUS2CALLBACKS structure pointer [Display Devices]","ddrawint/DD_MISCELLANEOUS2CALLBACKS","ddrawint/PDD_MISCELLANEOUS2CALLBACKS","ddstrcts_61459de1-283c-4693-a27a-f5dc8bdc5a44.xml","display.dd_miscellaneous2callbacks"]
old-location: display\dd_miscellaneous2callbacks.htm
tech.root: display
ms.assetid: bb3e91c0-5399-4760-a12e-0a47f0fbd2f9
ms.date: 12/05/2018
ms.keywords: '*PDD_MISCELLANEOUS2CALLBACKS, DD_MISCELLANEOUS2CALLBACKS, DD_MISCELLANEOUS2CALLBACKS structure [Display Devices], PDD_MISCELLANEOUS2CALLBACKS, PDD_MISCELLANEOUS2CALLBACKS structure pointer [Display Devices], ddrawint/DD_MISCELLANEOUS2CALLBACKS, ddrawint/PDD_MISCELLANEOUS2CALLBACKS, ddstrcts_61459de1-283c-4693-a27a-f5dc8bdc5a44.xml, display.dd_miscellaneous2callbacks'
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DD_MISCELLANEOUS2CALLBACKS, *PDD_MISCELLANEOUS2CALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_MISCELLANEOUS2CALLBACKS
 - ddrawint/_DD_MISCELLANEOUS2CALLBACKS
 - PDD_MISCELLANEOUS2CALLBACKS
 - ddrawint/PDD_MISCELLANEOUS2CALLBACKS
 - DD_MISCELLANEOUS2CALLBACKS
 - ddrawint/DD_MISCELLANEOUS2CALLBACKS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_MISCELLANEOUS2CALLBACKS
---

# DD_MISCELLANEOUS2CALLBACKS structure


## -description

The DD_MISCELLANEOUS2CALLBACKS structure is used to return the addresses of miscellaneous callback routines. These routines are new for Microsoft DirectX 7.0 and later and are exposed through <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> by responding to the GUID_Miscellaneous2Callbacks GUID.

## -struct-fields

### -field dwSize

Specifies the size, in bytes, of this structure.

### -field dwFlags

Indicates which miscellaneous callback functions the driver implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_MISC2CB32_CREATESURFACEEX</dt>
<dt>DDHAL_MISC2CB32_GETDRIVERSTATE</dt>
<dt>DDHAL_MISC2CB32_DESTROYDDLOCAL</dt>
</dl>

### -field AlphaBlt

Unused and must be set to <b>NULL</b>.

### -field CreateSurfaceEx

Points to the driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurfaceex">D3dCreateSurfaceEx</a> implementation. This callback creates an association between a DirectDraw surface and a small integer handle.

### -field GetDriverState

Points to the driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverstate">D3dGetDriverState</a> implementation.

### -field DestroyDDLocal

Points to the driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_destroyddlocal">D3dDestroyDDLocal</a> implementation. Used to destroy the local copy of the device context.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurfaceex">D3dCreateSurfaceEx</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_destroyddlocal">D3dDestroyDDLocal</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverstate">D3dGetDriverState</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>