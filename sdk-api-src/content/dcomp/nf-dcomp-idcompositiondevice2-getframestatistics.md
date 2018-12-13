---
UID: NF:dcomp.IDCompositionDevice2.GetFrameStatistics
title: IDCompositionDevice2::GetFrameStatistics
author: windows-sdk-content
description: Retrieves information from the composition engine about composition times and the frame rate.
old-location: directcomp\idcompositiondevice2_getframestatistics.htm
tech.root: directcomp
ms.assetid: 5C529575-46AC-495A-9165-15FC8F6B1F69
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFrameStatistics, GetFrameStatistics method [DirectComposition], GetFrameStatistics method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],GetFrameStatistics method, IDCompositionDevice2.GetFrameStatistics, IDCompositionDevice2::GetFrameStatistics, dcomp/IDCompositionDevice2::GetFrameStatistics, directcomp.idcompositiondevice2_getframestatistics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice2.GetFrameStatistics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice2::GetFrameStatistics


## -description


Retrieves information from the composition engine about composition times and the frame rate.


## -parameters




### -param statistics [out]

Type: <b><a href="https://msdn.microsoft.com/431D8399-9BCC-4B3A-89F4-E698446EF764">DCOMPOSITION_FRAME_STATISTICS</a>*</b>

A structure that receives composition times and frame rate information.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method retrieves timing information about the composition engine that an application can use to synchronize the rasterization of bitmaps with independent animations.




## -see-also




<a href="basic_concepts.htm">Composition Target Window</a>



<a href="https://msdn.microsoft.com/0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0">IDCompositionDevice2</a>
 

 

