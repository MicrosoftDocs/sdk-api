---
UID: NF:dcomp.IDCompositionDevice.GetFrameStatistics
title: IDCompositionDevice::GetFrameStatistics
author: windows-sdk-content
description: Retrieves information from the composition engine about composition times and the frame rate.
old-location: directcomp\idcompositiondevice_getframestatistics.htm
tech.root: directcomp
ms.assetid: C4DB7A16-BF91-4CD0-BCD2-4793D9599E0A
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetFrameStatistics, GetFrameStatistics method [DirectComposition], GetFrameStatistics method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],GetFrameStatistics method, IDCompositionDevice.GetFrameStatistics, IDCompositionDevice::GetFrameStatistics, dcomp/IDCompositionDevice::GetFrameStatistics, directcomp.idcompositiondevice_getframestatistics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IDCompositionDevice.GetFrameStatistics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice::GetFrameStatistics


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



<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>
 

 

