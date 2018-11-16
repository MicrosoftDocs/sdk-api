---
UID: NS:ddkmapi._DDGETVERSIONNUMBER
title: "_DDGETVERSIONNUMBER"
author: windows-sdk-content
description: The DDGETVERSIONNUMBER structure contains the version number of the kernel-mode video transport component of Microsoft DirectDraw that is supported by the video miniport driver's DxApi interface.
old-location: display\ddgetversionnumber.htm
tech.root: display
ms.assetid: fa752700-8bc4-46be-bed9-d7d546f18f03
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPDDGETVERSIONNUMBER, DDGETVERSIONNUMBER, DDGETVERSIONNUMBER structure [Display Devices], LPDDGETVERSIONNUMBER, LPDDGETVERSIONNUMBER structure pointer [Display Devices], _DDGETVERSIONNUMBER, ddkmapi/DDGETVERSIONNUMBER, ddkmapi/LPDDGETVERSIONNUMBER, ddstrcts_82a9e57e-1569-44f2-b903-41140e18621f.xml, display.ddgetversionnumber"
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
 - DDGETVERSIONNUMBER
product: Windows
targetos: Windows
req.typenames: DDGETVERSIONNUMBER, *LPDDGETVERSIONNUMBER
req.redist: 
---

# _DDGETVERSIONNUMBER structure


## -description


The DDGETVERSIONNUMBER structure contains the version number of the kernel-mode video transport component of Microsoft DirectDraw that is supported by the <a href="https://msdn.microsoft.com/3a540bfe-f340-4f12-acee-323b97683074">video miniport driver</a>'s <a href="https://msdn.microsoft.com/cfe77d14-32d2-44b7-8121-20ae7e4fe79e">DxApi interface</a>. 


## -struct-fields




### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a> function for <a href="https://msdn.microsoft.com/443892dc-293a-4355-9083-24715d08e619">DD_DXAPI_GETVERSIONNUMBER</a> operations. A return code of DD_OK indicates success.


### -field dwMajorVersion

Specifies the major version number (DXAPI_MAJORVERSION defined in <i>ddkmapi.h</i>).


### -field dwMinorVersion

Specifies the minor version number (DXAPI_MINORVERSION defined in <i>ddkmapi.h</i>).


## -see-also




<a href="https://msdn.microsoft.com/443892dc-293a-4355-9083-24715d08e619">DD_DXAPI_GETVERSIONNUMBER</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

