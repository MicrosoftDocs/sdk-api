---
UID: NS:ddkmapi._DDOPENVIDEOPORTIN
title: "_DDOPENVIDEOPORTIN"
author: windows-sdk-content
description: The DDOPENVIDEOPORTIN structure contains the video port extensions (VPE) object information.
old-location: display\ddopenvideoportin.htm
tech.root: display
ms.assetid: 53a0fdb3-583d-4da2-939c-6640ca9e6c31
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: "*LPDDOPENVIDEOPORTIN, DDOPENVIDEOPORTIN, DDOPENVIDEOPORTIN structure [Display Devices], LPDDOPENVIDEOPORTIN, LPDDOPENVIDEOPORTIN structure pointer [Display Devices], _DDOPENVIDEOPORTIN, ddkmapi/DDOPENVIDEOPORTIN, ddkmapi/LPDDOPENVIDEOPORTIN, ddstrcts_946323a4-8ead-46d5-aa18-2a3e1eaef2f1.xml, display.ddopenvideoportin"
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
 - DDOPENVIDEOPORTIN
product: Windows
targetos: Windows
req.typenames: DDOPENVIDEOPORTIN, *LPDDOPENVIDEOPORTIN
req.redist: 
---

# _DDOPENVIDEOPORTIN structure


## -description


The DDOPENVIDEOPORTIN structure contains the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object information. 


## -struct-fields




### -field hDirectDraw

Specifies the Microsoft DirectDraw object to which the surface handle is associated.


### -field dwVideoPortHandle

Specifies the hardware video port ID that was passed down when the VPE object was created in user mode.


### -field pfnVideoPortClose

Points to a <a href="https://msdn.microsoft.com/ee581d7b-c3b8-47e5-bae8-348b22ea0f95">pfnVideoPortClose</a> callback function that is called when the VPE object becomes unusable.


### -field pContext

Contains a value that is passed if the <b>pfnVideoPortClose</b> callback function is ever called.


## -see-also




<a href="https://msdn.microsoft.com/a54335f1-fc08-447a-ba65-f1d99ba7924d">DD_DXAPI_OPENVIDEOPORT</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

