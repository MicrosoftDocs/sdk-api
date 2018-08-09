---
UID: NS:ddrawint._DD_FLIPVPORTDATA
title: "_DD_FLIPVPORTDATA"
author: windows-sdk-content
description: The DD_FLIPVPORTDATA structure contains the information necessary for the video port extensions (VPE) object to perform a flip.
old-location: display\dd_flipvportdata.htm
old-project: display
ms.assetid: 1bc6dc12-1213-47d7-9e6f-2396a41cc6d0
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*PDD_FLIPVPORTDATA, DD_FLIPVPORTDATA, DD_FLIPVPORTDATA structure [Display Devices], _DD_FLIPVPORTDATA, ddrawint/DD_FLIPVPORTDATA, ddstrcts_9af598a7-a7fc-40f2-a1dd-355964f60da9.xml, display.dd_flipvportdata"
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
req.typenames: "*PDD_FLIPVPORTDATA, DD_FLIPVPORTDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_FLIPVPORTDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_FLIPVPORTDATA structure


## -description


The DD_FLIPVPORTDATA structure contains the information necessary for the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object to perform a flip.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only. 


### -field lpVideoPort

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551761">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object. 


### -field lpSurfCurr

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a>structure for the current surface; that is, the surface on which data is currently being written.


### -field lpSurfTarg

Points to a DD_SURFACE_LOCAL structure for the target surface; that is, the surface to which the driver should flip.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/1e31f33d-84da-40fa-a43c-30ad7d3055e8">DdVideoPortFlip</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field FlipVideoPort

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/1e31f33d-84da-40fa-a43c-30ad7d3055e8">DdVideoPortFlip</a>
 

 

