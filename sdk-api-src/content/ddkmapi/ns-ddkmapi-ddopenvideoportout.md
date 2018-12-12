---
UID: NS:ddkmapi._DDOPENVIDEOPORTOUT
title: DDOPENVIDEOPORTOUT
author: windows-sdk-content
description: The DDOPENVIDEOPORTOUT structure contains a Microsoft DirectDraw return code and a new surface handle if ddRVal is set to DD_OK. This new handle must be used on all subsequent calls that require a video port extensions (VPE) object handle.
old-location: display\ddopenvideoportout.htm
tech.root: display
ms.assetid: cb01786f-4e6a-43f6-b906-504c0f17ade7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDDOPENVIDEOPORTOUT, DDOPENVIDEOPORTOUT, DDOPENVIDEOPORTOUT structure [Display Devices], LPDDOPENVIDEOPORTOUT, LPDDOPENVIDEOPORTOUT structure pointer [Display Devices], ddkmapi/DDOPENVIDEOPORTOUT, ddkmapi/LPDDOPENVIDEOPORTOUT, ddstrcts_6a818660-2826-448a-a925-fa8019975c62.xml, display.ddopenvideoportout"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DDOPENVIDEOPORTOUT
product: Windows
targetos: Windows
req.typenames: DDOPENVIDEOPORTOUT, *LPDDOPENVIDEOPORTOUT
req.redist: 
---

# DDOPENVIDEOPORTOUT structure


## -description


The DDOPENVIDEOPORTOUT structure contains a Microsoft DirectDraw return code and a new surface handle if <b>ddRVal</b> is set to DD_OK. This new handle must be used on all subsequent calls that require a <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object handle. 


## -struct-fields




### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a> function for <a href="https://msdn.microsoft.com/a54335f1-fc08-447a-ba65-f1d99ba7924d">DD_DXAPI_OPENVIDEOPORT</a> operations. A return code of DD_OK indicates success.


### -field hVideoPort

Handle to the new VPE object.


## -see-also




<a href="https://msdn.microsoft.com/a54335f1-fc08-447a-ba65-f1d99ba7924d">DD_DXAPI_OPENVIDEOPORT</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

