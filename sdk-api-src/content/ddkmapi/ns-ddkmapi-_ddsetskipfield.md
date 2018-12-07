---
UID: NS:ddkmapi._DDSETSKIPFIELD
title: "_DDSETSKIPFIELD"
author: windows-sdk-content
description: The DDSETSKIPFIELD structure contains the start field information.
old-location: display\ddsetskipfield.htm
tech.root: display
ms.assetid: 146aa32d-5268-41b3-b98c-18223002ea65
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDDSETSKIPFIELD, DDSETSKIPFIELD, DDSETSKIPFIELD structure [Display Devices], LPDDSETSKIPFIELD, LPDDSETSKIPFIELD structure pointer [Display Devices], _DDSETSKIPFIELD, ddkmapi/DDSETSKIPFIELD, ddkmapi/LPDDSETSKIPFIELD, ddstrcts_a0567a56-5d6e-4154-86ff-90463ed2c554.xml, display.ddsetskipfield"
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
 - DDSETSKIPFIELD
product: Windows
targetos: Windows
req.typenames: DDSETSKIPFIELD, *LPDDSETSKIPFIELD
req.redist: 
---

# _DDSETSKIPFIELD structure


## -description


The DDSETSKIPFIELD structure contains the start field information. 


## -struct-fields




### -field hDirectDraw

Specifies the Microsoft DirectDraw handle.


### -field hVideoPort

Specifies the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object handle.


### -field dwStartField

Indicates the field that needs to be skipped and is relative to the current field. A value of 0 indicates it should skip the next field, a value of 1 indicates the field after that, and so on. 


## -see-also




<a href="https://msdn.microsoft.com/4ebab3bd-3290-4d09-a666-bf317755e715">DD_DXAPI_SET_VP_SKIP_FIELD</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

