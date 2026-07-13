---
UID: NS:ddkmapi._DDGETVERSIONNUMBER
title: DDGETVERSIONNUMBER (ddkmapi.h)
description: The DDGETVERSIONNUMBER structure contains the version number of the kernel-mode video transport component of Microsoft DirectDraw that is supported by the video miniport driver's DxApi interface.
helpviewer_keywords: ["*LPDDGETVERSIONNUMBER","DDGETVERSIONNUMBER","DDGETVERSIONNUMBER structure [Display Devices]","LPDDGETVERSIONNUMBER","LPDDGETVERSIONNUMBER structure pointer [Display Devices]","ddkmapi/DDGETVERSIONNUMBER","ddkmapi/LPDDGETVERSIONNUMBER","ddstrcts_82a9e57e-1569-44f2-b903-41140e18621f.xml","display.ddgetversionnumber"]
old-location: display\ddgetversionnumber.htm
tech.root: display
ms.assetid: fa752700-8bc4-46be-bed9-d7d546f18f03
ms.date: 12/05/2018
ms.keywords: '*LPDDGETVERSIONNUMBER, DDGETVERSIONNUMBER, DDGETVERSIONNUMBER structure [Display Devices], LPDDGETVERSIONNUMBER, LPDDGETVERSIONNUMBER structure pointer [Display Devices], ddkmapi/DDGETVERSIONNUMBER, ddkmapi/LPDDGETVERSIONNUMBER, ddstrcts_82a9e57e-1569-44f2-b903-41140e18621f.xml, display.ddgetversionnumber'
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
req.typenames: DDGETVERSIONNUMBER, *LPDDGETVERSIONNUMBER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETVERSIONNUMBER
 - ddkmapi/_DDGETVERSIONNUMBER
 - LPDDGETVERSIONNUMBER
 - ddkmapi/LPDDGETVERSIONNUMBER
 - DDGETVERSIONNUMBER
 - ddkmapi/DDGETVERSIONNUMBER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDGETVERSIONNUMBER
---

# DDGETVERSIONNUMBER structure


## -description

The DDGETVERSIONNUMBER structure contains the version number of the kernel-mode video transport component of Microsoft DirectDraw that is supported by the <a href="/windows-hardware/drivers/display/video-miniport-drivers-in-the-windows-2000-display-driver-model">video miniport driver</a>'s <a href="/windows-hardware/drivers/ddi/content/index">DxApi interface</a>.

## -struct-fields

### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function for <a href="/previous-versions/windows/hardware/drivers/ff550637(v=vs.85)">DD_DXAPI_GETVERSIONNUMBER</a> operations. A return code of DD_OK indicates success.

### -field dwMajorVersion

Specifies the major version number (DXAPI_MAJORVERSION defined in <i>ddkmapi.h</i>).

### -field dwMinorVersion

Specifies the minor version number (DXAPI_MINORVERSION defined in <i>ddkmapi.h</i>).

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550637(v=vs.85)">DD_DXAPI_GETVERSIONNUMBER</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>