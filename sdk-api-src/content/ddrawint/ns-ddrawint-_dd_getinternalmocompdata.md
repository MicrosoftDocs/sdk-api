---
UID: NS:ddrawint._DD_GETINTERNALMOCOMPDATA
title: "_DD_GETINTERNALMOCOMPDATA"
author: windows-sdk-content
description: The DD_GETINTERNALMOCOMPDATA structure contains the internal memory requirements.
old-location: display\dd_getinternalmocompdata.htm
old-project: display
ms.assetid: 5d8f722f-7574-485e-9ff2-568cd0ae23f7
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PDD_GETINTERNALMOCOMPDATA, DD_GETINTERNALMOCOMPDATA, DD_GETINTERNALMOCOMPDATA structure [Display Devices], _DD_GETINTERNALMOCOMPDATA, ddrawint/DD_GETINTERNALMOCOMPDATA, ddstrcts_02721b17-cf19-462c-b588-039431b8d548.xml, display.dd_getinternalmocompdata"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
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
req.typenames: "*PDD_GETINTERNALMOCOMPDATA, DD_GETINTERNALMOCOMPDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_GETINTERNALMOCOMPDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_GETINTERNALMOCOMPDATA structure


## -description


The DD_GETINTERNALMOCOMPDATA structure contains the internal memory requirements. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpGuid

Points to a GUID for which the internal memory requirement is requested. 


### -field dwWidth

Indicates the width in pixels of uncompressed output frame.


### -field dwHeight

Indicates the height in pixels of uncompressed output frame.


### -field ddPixelFormat

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a> structure that contains the pixel format of the uncompressed output frame.


### -field dwScratchMemAlloc

Indicates the size in bytes of internal memory that the display driver privately reserves to perform motion compensation 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/297ff4a2-52f4-4b24-9abe-9c7d22a9b3ad">DdMoCompGetInternalInfo</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/297ff4a2-52f4-4b24-9abe-9c7d22a9b3ad">DdMoCompGetInternalInfo</a>
 

 

