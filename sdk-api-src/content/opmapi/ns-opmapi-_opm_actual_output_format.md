---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _OPM_ACTUAL_OUTPUT_FORMAT structure


## -description


Contains the result of an <a href="https://msdn.microsoft.com/8464470f-49db-4559-80b2-02cfc473e30e">OPM_GET_ACTUAL_OUTPUT_FORMAT</a> query in <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a> (OPM). 


## -struct-fields




### -field rnRandomNumber

An <a href="https://msdn.microsoft.com/d3a5be4b-39d1-43da-b87e-ab4dd7815262">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="https://msdn.microsoft.com/8959c7d1-9a78-497f-8841-d3e61e9db6a3">OPM_GET_INFO_PARAMETERS</a> or <a href="https://msdn.microsoft.com/46c0c426-9730-4a0e-ab95-03b240bd55f0">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure.


### -field ulStatusFlags

A bitwise <b>OR</b> of <a href="https://msdn.microsoft.com/d6d85fd4-e735-4610-93e0-bb2b1782f11b">OPM Status Flags</a>.


### -field ulDisplayWidth

The width of the display mode, in pixels.


### -field ulDisplayHeight

The height of the display mode, in pixels.


### -field dsfSampleInterleaveFormat

A <a href="https://msdn.microsoft.com/7d2d38c0-249d-47c3-acda-ba1bec721a5c">DXVA2_SampleFormat</a> value that describes the interlace mode.


### -field d3dFormat

A <b>D3DFORMAT</b> value that describes the video format.


### -field ulFrequencyNumerator

The numerator of the refresh rate of the current display mode.


### -field ulFrequencyDenominator

The denominator of the refresh rate of the current display mode.


## -remarks



The refresh rate is expressed as a fraction. For example, if the refresh rate is 72 Hz, <b>FreqNumerator</b> = 72 and <b>FreqDenominator</b> = 1. For NTSC television, the values are <b>FreqNumerator</b> = 60000 and <b>FreqDenominator</b> = 1001 (59.94 fields per second). 

The layout of this structure is identical to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563157">DXVA_COPPStatusDisplayData</a> structure used in Certified Output Protection Protocol (COPP).




## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

