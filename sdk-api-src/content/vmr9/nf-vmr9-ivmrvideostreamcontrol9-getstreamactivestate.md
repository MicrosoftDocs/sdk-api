---
UID: NF:vmr9.IVMRVideoStreamControl9.GetStreamActiveState
title: IVMRVideoStreamControl9::GetStreamActiveState
author: windows-sdk-content
description: The GetStreamActiveState method retrieves the state of the stream.
old-location: dshow\ivmrvideostreamcontrol9_getstreamactivestate.htm
tech.root: DirectShow
ms.assetid: db6637ec-de60-434f-be97-ce27ad02e627
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetStreamActiveState, GetStreamActiveState method [DirectShow], GetStreamActiveState method [DirectShow],IVMRVideoStreamControl9 interface, IVMRVideoStreamControl9 interface [DirectShow],GetStreamActiveState method, IVMRVideoStreamControl9.GetStreamActiveState, IVMRVideoStreamControl9::GetStreamActiveState, IVMRVideoStreamControl9GetStreamActiveState, dshow.ivmrvideostreamcontrol9_getstreamactivestate, vmr9/IVMRVideoStreamControl9::GetStreamActiveState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRVideoStreamControl9.GetStreamActiveState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vmr9.h
: 
- IVMRVideoStreamControl9.GetStreamActiveState
: 
---

# IVMRVideoStreamControl9::GetStreamActiveState


## -description



The <code>GetStreamActiveState</code> method retrieves the state of the stream.




## -parameters




### -param lpfActive [out]

Receives the current state of the stream. <b>TRUE</b> means the stream is active; <b>FALSE</b> means that it is inactive.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/df642ebb-058b-41db-95d3-d7d3bf9a6dd0">IVMRVideoStreamControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

