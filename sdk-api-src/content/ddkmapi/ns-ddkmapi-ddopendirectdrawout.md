---
UID: NS:ddkmapi._DDOPENDIRECTDRAWOUT
title: DDOPENDIRECTDRAWOUT (ddkmapi.h)
author: windows-sdk-content
description: The DDOPENDIRECTDRAWOUT structure contains a new Microsoft DirectDraw handle for the DD_DXAPI_OPENDIRECTDRAW function identifier of the DxApi function if the ddRVal member of DDOPENDIRECTDRAWOUT is set to DD_OK.
old-location: display\ddopendirectdrawout.htm
tech.root: display
ms.assetid: 49fa1354-2b66-4e97-a8e6-aa7c995d6628
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDDOPENDIRECTDRAWOUT, DDOPENDIRECTDRAWOUT, DDOPENDIRECTDRAWOUT structure [Display Devices], LPDDOPENDIRECTDRAWOUT, LPDDOPENDIRECTDRAWOUT structure pointer [Display Devices], ddkmapi/DDOPENDIRECTDRAWOUT, ddkmapi/LPDDOPENDIRECTDRAWOUT, ddstrcts_26b6b5d6-563a-4d01-b2f5-dc984b8d382e.xml, display.ddopendirectdrawout"
ms.topic: struct
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
 - DDOPENDIRECTDRAWOUT
product: Windows
targetos: Windows
req.typenames: DDOPENDIRECTDRAWOUT, *LPDDOPENDIRECTDRAWOUT
req.redist: 
ms.custom: 19H1
---

# DDOPENDIRECTDRAWOUT structure


## -description


The DDOPENDIRECTDRAWOUT structure contains a new Microsoft DirectDraw handle for the <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550702(v=vs.85)">DD_DXAPI_OPENDIRECTDRAW</a> function identifier of the <b>DxApi</b> function if the <b>ddRVal</b> member of DDOPENDIRECTDRAWOUT is set to DD_OK. This new handle must be used on all subsequent calls that require a DirectDraw handle. 


## -struct-fields




### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/dxapi/nf-dxapi-dxapi">DxApi</a> function for <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550702(v=vs.85)">DD_DXAPI_OPENDIRECTDRAW</a> operations. A return code of DD_OK indicates success.


### -field hDirectDraw

Handle to the new DirectDraw object.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550702(v=vs.85)">DD_DXAPI_OPENDIRECTDRAW</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/dxapi/nf-dxapi-dxapi">DxApi</a>
 

 

