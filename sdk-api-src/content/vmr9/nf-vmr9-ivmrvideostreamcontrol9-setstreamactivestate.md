---
UID: NF:vmr9.IVMRVideoStreamControl9.SetStreamActiveState
title: IVMRVideoStreamControl9::SetStreamActiveState
author: windows-sdk-content
description: The SetStreamActiveState method activates or inactivates an input stream.
old-location: dshow\ivmrvideostreamcontrol9_setstreamactivestate.htm
tech.root: DirectShow
ms.assetid: 2c17a006-f086-49cd-a237-3713fb9bd3f9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVMRVideoStreamControl9 interface [DirectShow],SetStreamActiveState method, IVMRVideoStreamControl9.SetStreamActiveState, IVMRVideoStreamControl9::SetStreamActiveState, IVMRVideoStreamControl9SetStreamActiveState, SetStreamActiveState, SetStreamActiveState method [DirectShow], SetStreamActiveState method [DirectShow],IVMRVideoStreamControl9 interface, dshow.ivmrvideostreamcontrol9_setstreamactivestate, vmr9/IVMRVideoStreamControl9::SetStreamActiveState
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
 - IVMRVideoStreamControl9.SetStreamActiveState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRVideoStreamControl9::SetStreamActiveState


## -description



The <code>SetStreamActiveState</code> method activates or inactivates an input stream.




## -parameters




### -param fActive [in]

Specifies the state of the stream. <b>TRUE</b> means active; <b>FALSE</b> means inactive.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/df642ebb-058b-41db-95d3-d7d3bf9a6dd0">IVMRVideoStreamControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

