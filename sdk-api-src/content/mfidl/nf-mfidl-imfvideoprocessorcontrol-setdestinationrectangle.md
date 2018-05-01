---
UID: NF:mfidl.IMFVideoProcessorControl.SetDestinationRectangle
title: IMFVideoProcessorControl::SetDestinationRectangle method
author: windows-driver-content
description: Sets the destination rectangle.
old-location: mf\imfvideoprocessorcontrol_setdestinationrectangle.htm
old-project: medfound
ms.assetid: 8AD1BDF4-2508-4A99-85A1-9DBC969D511B
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFVideoProcessorControl, IMFVideoProcessorControl interface [Media Foundation], SetDestinationRectangle method, IMFVideoProcessorControl::SetDestinationRectangle, SetDestinationRectangle method [Media Foundation], SetDestinationRectangle method [Media Foundation], IMFVideoProcessorControl interface, SetDestinationRectangle,IMFVideoProcessorControl.SetDestinationRectangle, mf.imfvideoprocessorcontrol_setdestinationrectangle, mfidl/IMFVideoProcessorControl::SetDestinationRectangle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFVideoProcessorControl.SetDestinationRectangle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoProcessorControl::SetDestinationRectangle method


## -description


Sets the destination rectangle. The destination rectangle is the portion of the output surface where the source rectangle is blitted.


## -parameters




### -param pDstRect

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the destination rectangle.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



See <a href="https://msdn.microsoft.com/1476995A-9692-4B08-8EF7-7DB6321BEC24">Video Processor MFT</a> for info regarding source and destination rectangles in the <b>Video Processor MFT</b>.   




## -see-also




<a href="https://msdn.microsoft.com/6803B69E-CF84-45D5-804C-BD961BD5E13D">IMFVideoProcessorControl</a>
 

 

