---
UID: NS:ddkmapi._DDSETSKIPFIELD
title: DDSETSKIPFIELD (ddkmapi.h)
description: The DDSETSKIPFIELD structure contains the start field information.
helpviewer_keywords: ["*LPDDSETSKIPFIELD","DDSETSKIPFIELD","DDSETSKIPFIELD structure [Display Devices]","LPDDSETSKIPFIELD","LPDDSETSKIPFIELD structure pointer [Display Devices]","ddkmapi/DDSETSKIPFIELD","ddkmapi/LPDDSETSKIPFIELD","ddstrcts_a0567a56-5d6e-4154-86ff-90463ed2c554.xml","display.ddsetskipfield"]
old-location: display\ddsetskipfield.htm
tech.root: display
ms.assetid: 146aa32d-5268-41b3-b98c-18223002ea65
ms.date: 12/05/2018
ms.keywords: '*LPDDSETSKIPFIELD, DDSETSKIPFIELD, DDSETSKIPFIELD structure [Display Devices], LPDDSETSKIPFIELD, LPDDSETSKIPFIELD structure pointer [Display Devices], ddkmapi/DDSETSKIPFIELD, ddkmapi/LPDDSETSKIPFIELD, ddstrcts_a0567a56-5d6e-4154-86ff-90463ed2c554.xml, display.ddsetskipfield'
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
req.typenames: DDSETSKIPFIELD, *LPDDSETSKIPFIELD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDSETSKIPFIELD
 - ddkmapi/_DDSETSKIPFIELD
 - LPDDSETSKIPFIELD
 - ddkmapi/LPDDSETSKIPFIELD
 - DDSETSKIPFIELD
 - ddkmapi/DDSETSKIPFIELD
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
 - DDSETSKIPFIELD
---

# DDSETSKIPFIELD structure


## -description

The DDSETSKIPFIELD structure contains the start field information.

## -struct-fields

### -field hDirectDraw

Specifies the Microsoft DirectDraw handle.

### -field hVideoPort

Specifies the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object handle.

### -field dwStartField

Indicates the field that needs to be skipped and is relative to the current field. A value of 0 indicates it should skip the next field, a value of 1 indicates the field after that, and so on.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff551510(v=vs.85)">DD_DXAPI_SET_VP_SKIP_FIELD</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>