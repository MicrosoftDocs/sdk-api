---
UID: NS:ddkmapi._DDOPENVPCAPTUREDEVICEOUT
title: "_DDOPENVPCAPTUREDEVICEOUT"
author: windows-sdk-content
description: The DDOPENVPCAPTUREDEVICEOUT structure contains the video port extensions (VPE) capture handle.
old-location: display\ddopenvpcapturedeviceout.htm
old-project: display
ms.assetid: 5979ccd5-7c35-4088-96b3-15e4416d5471
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*LPDDOPENVPCAPTUREDEVICEOUT, DDOPENVPCAPTUREDEVICEOUT, DDOPENVPCAPTUREDEVICEOUT structure [Display Devices], LPDDOPENVPCAPTUREDEVICEOUT, LPDDOPENVPCAPTUREDEVICEOUT structure pointer [Display Devices], _DDOPENVPCAPTUREDEVICEOUT, ddkmapi/DDOPENVPCAPTUREDEVICEOUT, ddkmapi/LPDDOPENVPCAPTUREDEVICEOUT, ddstrcts_b477f183-6c80-47db-a9ee-5bcbe7162774.xml, display.ddopenvpcapturedeviceout"
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
req.typenames: DDOPENVPCAPTUREDEVICEOUT, *LPDDOPENVPCAPTUREDEVICEOUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDOPENVPCAPTUREDEVICEOUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DDOPENVPCAPTUREDEVICEOUT structure


## -description


The DDOPENVPCAPTUREDEVICEOUT structure contains the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> capture handle. 


## -struct-fields




### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function for <a href="https://msdn.microsoft.com/library/windows/hardware/ff551500">DD_DXAPI_OPENVPCAPTUREDEVICE</a> operations. A return code of DD_OK indicates success.


### -field hCapture

Handle to the new VPE capture object.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551500">DD_DXAPI_OPENVPCAPTUREDEVICE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

