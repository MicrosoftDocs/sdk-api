---
UID: NS:ddkmapi._DDOPENVIDEOPORTOUT
title: DDOPENVIDEOPORTOUT (ddkmapi.h)

description: The DDOPENVIDEOPORTOUT structure contains a Microsoft DirectDraw return code and a new surface handle if ddRVal is set to DD_OK. This new handle must be used on all subsequent calls that require a video port extensions (VPE) object handle.
old-location: display\ddopenvideoportout.htm
tech.root: display
ms.assetid: cb01786f-4e6a-43f6-b906-504c0f17ade7

ms.date: 12/05/2018
ms.keywords: "*LPDDOPENVIDEOPORTOUT, DDOPENVIDEOPORTOUT, DDOPENVIDEOPORTOUT structure [Display Devices], LPDDOPENVIDEOPORTOUT, LPDDOPENVIDEOPORTOUT structure pointer [Display Devices], ddkmapi/DDOPENVIDEOPORTOUT, ddkmapi/LPDDOPENVIDEOPORTOUT, ddstrcts_6a818660-2826-448a-a925-fa8019975c62.xml, display.ddopenvideoportout"
ms.topic: struct
f1_keywords: 
 - "ddkmapi/DDOPENVIDEOPORTOUT"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDOPENVIDEOPORTOUT
targetos: Windows
req.typenames: DDOPENVIDEOPORTOUT, *LPDDOPENVIDEOPORTOUT
req.redist: 
ms.custom: 19H1
---

# DDOPENVIDEOPORTOUT structure


## -description


The DDOPENVIDEOPORTOUT structure contains a Microsoft DirectDraw return code and a new surface handle if <b>ddRVal</b> is set to DD_OK. This new handle must be used on all subsequent calls that require a <a href="https://docs.microsoft.com/windows-hardware/drivers/">video port extensions (VPE)</a> object handle. 


## -struct-fields




### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/dxapi/nf-dxapi-dxapi">DxApi</a> function for <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff551498(v=vs.85)">DD_DXAPI_OPENVIDEOPORT</a> operations. A return code of DD_OK indicates success.


### -field hVideoPort

Handle to the new VPE object.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff551498(v=vs.85)">DD_DXAPI_OPENVIDEOPORT</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/dxapi/nf-dxapi-dxapi">DxApi</a>
 

 

