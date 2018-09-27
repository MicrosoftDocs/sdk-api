---
UID: NS:dxva9typ._DXVA_COPPStatusDisplayData
title: "_DXVA_COPPStatusDisplayData"
author: windows-sdk-content
description: Contains the result of a Display Data query in Certified Output Protection Protocol (COPP).
old-location: dshow\dxva_coppstatusdisplaydata.htm
tech.root: DirectShow
ms.assetid: 51a119a0-d5de-4df0-9c2b-c776e9af8c60
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DXVA_COPPStatusDisplayData, DXVA_COPPStatusDisplayData structure [DirectShow], DXVA_COPPStatusDisplayDataStructure, _DXVA_COPPStatusDisplayData, dshow.dxva_coppstatusdisplaydata, dxva9typ/DXVA_COPPStatusDisplayData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxva9typ.h
req.include-header: Dxva.h
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
 - dxva9typ.h
api_name:
 - DXVA_COPPStatusDisplayData
product: Windows
targetos: Windows
req.typenames: DXVA_COPPStatusDisplayData
req.redist: 
---

# _DXVA_COPPStatusDisplayData structure


## -description



Contains the result of a Display Data query in Certified Output Protection Protocol (COPP).




## -struct-fields




### -field rApp

A 128-bit random number that was passed by the application in the <a href="https://msdn.microsoft.com/988e6d54-f241-4cfc-8793-fc42de92ac52">AMCOPPStatusInput</a> structure.


### -field dwFlags

Status flag. See <a href="https://msdn.microsoft.com/9109bb2c-1422-4629-b2df-ac877d3cd86e">COPP_StatusFlags</a>.


### -field DisplayWidth

Width of the display mode, in pixels.


### -field DisplayHeight

Height of the display mode, in pixels.


### -field Format

Contains a <b>DXVA_ExtendedFormat</b> structure packed into a <b>ULONG</b>, describing the video format.


### -field d3dFormat

Contains a <b>D3DFORMAT</b> value that describes the video format. For more information, see the Direct3D SDK documentation.


### -field FreqNumerator

The numerator of the refresh rate of the current display mode.


### -field FreqDenominator

The denominator of the refresh rate of the current display mode.


## -remarks



The refresh rate is expressed as a fraction. For example, if the refresh rate is 72 Hz, <b>FreqNumerator</b> = 72 and <b>FreqDenominator</b> = 1. For NTSC television, the values are <b>FreqNumerator</b> = 60000 and <b>FreqDenominator</b> = 1001 (59.94 fields per second).




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

