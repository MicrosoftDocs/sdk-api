---
UID: NS:winddi._FD_XFORM
title: "_FD_XFORM"
author: windows-sdk-content
description: The FD_XFORM structure describes an arbitrary two-dimensional font transform.
old-location: display\fd_xform.htm
tech.root: display
ms.assetid: 4d15a771-fbf2-46ed-9698-faa3840f5f76
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*PFD_XFORM, FD_XFORM, FD_XFORM structure [Display Devices], PFD_XFORM, PFD_XFORM structure pointer [Display Devices], _FD_XFORM, display.fd_xform, grstrcts_c68b9048-8da3-4c5d-b977-6bd50cbd6703.xml, winddi/FD_XFORM, winddi/PFD_XFORM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: 
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
 - winddi.h
api_name:
 - FD_XFORM
product: Windows
targetos: Windows
req.typenames: FD_XFORM, *PFD_XFORM
req.redist: 
---

# _FD_XFORM structure


## -description


The FD_XFORM structure describes an arbitrary two-dimensional font transform. 


## -struct-fields




### -field eXX


### -field eXY


### -field eYX


### -field eYY

Are the four elements that comprise a 2x2 row-major matrix. <b>eXX</b> and <b>eXY</b> are the elements in the first row; <b>eYX</b> and <b>eYY</b> are the elements in the second row.


## -remarks



This structure is used typically to hold notional-to-device-space font transformations.



