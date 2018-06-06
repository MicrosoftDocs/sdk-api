---
UID: NS:ddkmapi._DDOPENDIRECTDRAWOUT
title: "_DDOPENDIRECTDRAWOUT"
author: windows-sdk-content
description: The DDOPENDIRECTDRAWOUT structure contains a new Microsoft DirectDraw handle for the DD_DXAPI_OPENDIRECTDRAW function identifier of the DxApi function if the ddRVal member of DDOPENDIRECTDRAWOUT is set to DD_OK.
old-location: display\ddopendirectdrawout.htm
old-project: display
ms.assetid: 49fa1354-2b66-4e97-a8e6-aa7c995d6628
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*LPDDOPENDIRECTDRAWOUT, DDOPENDIRECTDRAWOUT, DDOPENDIRECTDRAWOUT structure [Display Devices], LPDDOPENDIRECTDRAWOUT, LPDDOPENDIRECTDRAWOUT structure pointer [Display Devices], _DDOPENDIRECTDRAWOUT, ddkmapi/DDOPENDIRECTDRAWOUT, ddkmapi/LPDDOPENDIRECTDRAWOUT, ddstrcts_26b6b5d6-563a-4d01-b2f5-dc984b8d382e.xml, display.ddopendirectdrawout"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DDOPENDIRECTDRAWOUT, *LPDDOPENDIRECTDRAWOUT
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
req.lib: 
req.dll: 
req.irql: 
---

# _DDOPENDIRECTDRAWOUT structure


## -description


The DDOPENDIRECTDRAWOUT structure contains a new Microsoft DirectDraw handle for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550702">DD_DXAPI_OPENDIRECTDRAW</a> function identifier of the <b>DxApi</b> function if the <b>ddRVal</b> member of DDOPENDIRECTDRAWOUT is set to DD_OK. This new handle must be used on all subsequent calls that require a DirectDraw handle. 


## -struct-fields




### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function for <a href="https://msdn.microsoft.com/library/windows/hardware/ff550702">DD_DXAPI_OPENDIRECTDRAW</a> operations. A return code of DD_OK indicates success.


### -field hDirectDraw

Handle to the new DirectDraw object.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550702">DD_DXAPI_OPENDIRECTDRAW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

