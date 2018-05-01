---
UID: NF:strmif.IVMRVideoStreamControl.GetStreamActiveState
title: IVMRVideoStreamControl::GetStreamActiveState method
author: windows-driver-content
description: The GetStreamActiveState method retrieves the state of the stream.
old-location: dshow\ivmrvideostreamcontrol_getstreamactivestate.htm
old-project: DirectShow
ms.assetid: 619ba669-c2a0-46fe-9c12-52105b107351
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetStreamActiveState method [DirectShow], GetStreamActiveState method [DirectShow], IVMRVideoStreamControl interface, GetStreamActiveState,IVMRVideoStreamControl.GetStreamActiveState, IVMRVideoStreamControl, IVMRVideoStreamControl interface [DirectShow], GetStreamActiveState method, IVMRVideoStreamControl::GetStreamActiveState, IVMRVideoStreamControlGetStreamActiveState, dshow.ivmrvideostreamcontrol_getstreamactivestate, strmif/IVMRVideoStreamControl::GetStreamActiveState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRVideoStreamControl.GetStreamActiveState
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRVideoStreamControl::GetStreamActiveState method


## -description



The <code>GetStreamActiveState</code> method retrieves the state of the stream.




## -parameters




### -param lpfActive [out]

Receives the current state of the stream. <b>TRUE</b> means the stream is active; <b>FALSE</b> means that it is inactive.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/b42fa81e-99d7-4051-b909-2189581825d0">IVMRVideoStreamControl Interface</a>



<a href="https://msdn.microsoft.com/060a95a4-b984-40c6-afe8-136df96c353e">IVMRVideoStreamControl::SetStreamActiveState</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

