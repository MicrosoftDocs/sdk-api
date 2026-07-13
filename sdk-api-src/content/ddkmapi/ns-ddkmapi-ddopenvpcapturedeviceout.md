---
UID: NS:ddkmapi._DDOPENVPCAPTUREDEVICEOUT
title: DDOPENVPCAPTUREDEVICEOUT (ddkmapi.h)
description: The DDOPENVPCAPTUREDEVICEOUT structure contains the video port extensions (VPE) capture handle.
helpviewer_keywords: ["*LPDDOPENVPCAPTUREDEVICEOUT","DDOPENVPCAPTUREDEVICEOUT","DDOPENVPCAPTUREDEVICEOUT structure [Display Devices]","LPDDOPENVPCAPTUREDEVICEOUT","LPDDOPENVPCAPTUREDEVICEOUT structure pointer [Display Devices]","ddkmapi/DDOPENVPCAPTUREDEVICEOUT","ddkmapi/LPDDOPENVPCAPTUREDEVICEOUT","ddstrcts_b477f183-6c80-47db-a9ee-5bcbe7162774.xml","display.ddopenvpcapturedeviceout"]
old-location: display\ddopenvpcapturedeviceout.htm
tech.root: display
ms.assetid: 5979ccd5-7c35-4088-96b3-15e4416d5471
ms.date: 12/05/2018
ms.keywords: '*LPDDOPENVPCAPTUREDEVICEOUT, DDOPENVPCAPTUREDEVICEOUT, DDOPENVPCAPTUREDEVICEOUT structure [Display Devices], LPDDOPENVPCAPTUREDEVICEOUT, LPDDOPENVPCAPTUREDEVICEOUT structure pointer [Display Devices], ddkmapi/DDOPENVPCAPTUREDEVICEOUT, ddkmapi/LPDDOPENVPCAPTUREDEVICEOUT, ddstrcts_b477f183-6c80-47db-a9ee-5bcbe7162774.xml, display.ddopenvpcapturedeviceout'
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
req.typenames: DDOPENVPCAPTUREDEVICEOUT, *LPDDOPENVPCAPTUREDEVICEOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDOPENVPCAPTUREDEVICEOUT
 - ddkmapi/_DDOPENVPCAPTUREDEVICEOUT
 - LPDDOPENVPCAPTUREDEVICEOUT
 - ddkmapi/LPDDOPENVPCAPTUREDEVICEOUT
 - DDOPENVPCAPTUREDEVICEOUT
 - ddkmapi/DDOPENVPCAPTUREDEVICEOUT
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
 - DDOPENVPCAPTUREDEVICEOUT
---

# DDOPENVPCAPTUREDEVICEOUT structure


## -description

The DDOPENVPCAPTUREDEVICEOUT structure contains the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> capture handle.

## -struct-fields

### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function for <a href="/previous-versions/windows/hardware/drivers/ff551500(v=vs.85)">DD_DXAPI_OPENVPCAPTUREDEVICE</a> operations. A return code of DD_OK indicates success.

### -field hCapture

Handle to the new VPE capture object.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff551500(v=vs.85)">DD_DXAPI_OPENVPCAPTUREDEVICE</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>