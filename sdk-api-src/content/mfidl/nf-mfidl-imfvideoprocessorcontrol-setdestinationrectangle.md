---
UID: NF:mfidl.IMFVideoProcessorControl.SetDestinationRectangle
title: IMFVideoProcessorControl::SetDestinationRectangle (mfidl.h)
author: windows-sdk-content
description: Sets the destination rectangle.
old-location: mf\imfvideoprocessorcontrol_setdestinationrectangle.htm
tech.root: medfound
ms.assetid: 8AD1BDF4-2508-4A99-85A1-9DBC969D511B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessorControl interface [Media Foundation],SetDestinationRectangle method, IMFVideoProcessorControl.SetDestinationRectangle, IMFVideoProcessorControl::SetDestinationRectangle, SetDestinationRectangle, SetDestinationRectangle method [Media Foundation], SetDestinationRectangle method [Media Foundation],IMFVideoProcessorControl interface, mf.imfvideoprocessorcontrol_setdestinationrectangle, mfidl/IMFVideoProcessorControl::SetDestinationRectangle
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl.SetDestinationRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoProcessorControl::SetDestinationRectangle


## -description


Sets the destination rectangle. The destination rectangle is the portion of the output surface where the source rectangle is blitted.


## -parameters




### -param pDstRect

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the destination rectangle.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



See <a href="https://msdn.microsoft.com/1476995A-9692-4B08-8EF7-7DB6321BEC24">Video Processor MFT</a> for info regarding source and destination rectangles in the <b>Video Processor MFT</b>.   




## -see-also




<a href="https://msdn.microsoft.com/6803B69E-CF84-45D5-804C-BD961BD5E13D">IMFVideoProcessorControl</a>
 

 

