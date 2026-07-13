---
UID: NS:ddkmapi._DDOPENVIDEOPORTIN
title: DDOPENVIDEOPORTIN (ddkmapi.h)
description: The DDOPENVIDEOPORTIN structure contains the video port extensions (VPE) object information.
helpviewer_keywords: ["*LPDDOPENVIDEOPORTIN","DDOPENVIDEOPORTIN","DDOPENVIDEOPORTIN structure [Display Devices]","LPDDOPENVIDEOPORTIN","LPDDOPENVIDEOPORTIN structure pointer [Display Devices]","ddkmapi/DDOPENVIDEOPORTIN","ddkmapi/LPDDOPENVIDEOPORTIN","ddstrcts_946323a4-8ead-46d5-aa18-2a3e1eaef2f1.xml","display.ddopenvideoportin"]
old-location: display\ddopenvideoportin.htm
tech.root: display
ms.assetid: 53a0fdb3-583d-4da2-939c-6640ca9e6c31
ms.date: 12/05/2018
ms.keywords: '*LPDDOPENVIDEOPORTIN, DDOPENVIDEOPORTIN, DDOPENVIDEOPORTIN structure [Display Devices], LPDDOPENVIDEOPORTIN, LPDDOPENVIDEOPORTIN structure pointer [Display Devices], ddkmapi/DDOPENVIDEOPORTIN, ddkmapi/LPDDOPENVIDEOPORTIN, ddstrcts_946323a4-8ead-46d5-aa18-2a3e1eaef2f1.xml, display.ddopenvideoportin'
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
req.typenames: DDOPENVIDEOPORTIN, *LPDDOPENVIDEOPORTIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDOPENVIDEOPORTIN
 - ddkmapi/_DDOPENVIDEOPORTIN
 - LPDDOPENVIDEOPORTIN
 - ddkmapi/LPDDOPENVIDEOPORTIN
 - DDOPENVIDEOPORTIN
 - ddkmapi/DDOPENVIDEOPORTIN
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
 - DDOPENVIDEOPORTIN
---

# DDOPENVIDEOPORTIN structure


## -description

The DDOPENVIDEOPORTIN structure contains the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object information.

## -struct-fields

### -field hDirectDraw

Specifies the Microsoft DirectDraw object to which the surface handle is associated.

### -field dwVideoPortHandle

Specifies the hardware video port ID that was passed down when the VPE object was created in user mode.

### -field pfnVideoPortClose

Points to a <a href="/windows/desktop/api/ddkmapi/nc-ddkmapi-lpdd_notifycallback">pfnVideoPortClose</a> callback function that is called when the VPE object becomes unusable.

### -field pContext

Contains a value that is passed if the <b>pfnVideoPortClose</b> callback function is ever called.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff551498(v=vs.85)">DD_DXAPI_OPENVIDEOPORT</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>