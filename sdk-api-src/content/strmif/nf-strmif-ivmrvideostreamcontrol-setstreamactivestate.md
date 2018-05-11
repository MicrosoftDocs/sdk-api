---
UID: NF:strmif.IVMRVideoStreamControl.SetStreamActiveState
title: IVMRVideoStreamControl::SetStreamActiveState
author: windows-driver-content
description: The SetStreamActiveState method activates or inactivates an input stream.
old-location: dshow\ivmrvideostreamcontrol_setstreamactivestate.htm
old-project: DirectShow
ms.assetid: 060a95a4-b984-40c6-afe8-136df96c353e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IVMRVideoStreamControl interface [DirectShow],SetStreamActiveState method, IVMRVideoStreamControl.SetStreamActiveState, IVMRVideoStreamControl::SetStreamActiveState, IVMRVideoStreamControlSetStreamActiveState, SetStreamActiveState, SetStreamActiveState method [DirectShow], SetStreamActiveState method [DirectShow],IVMRVideoStreamControl interface, dshow.ivmrvideostreamcontrol_setstreamactivestate, strmif/IVMRVideoStreamControl::SetStreamActiveState
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
-	IVMRVideoStreamControl.SetStreamActiveState
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRVideoStreamControl::SetStreamActiveState


## -description



The <code>SetStreamActiveState</code> method activates or inactivates an input stream.




## -parameters




### -param fActive [in]

Specifies the state of the stream. <b>TRUE</b> means active; <b>FALSE</b> means inactive.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/b42fa81e-99d7-4051-b909-2189581825d0">IVMRVideoStreamControl Interface</a>



<a href="https://msdn.microsoft.com/619ba669-c2a0-46fe-9c12-52105b107351">IVMRVideoStreamControl::GetStreamActiveState</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

