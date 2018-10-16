---
UID: NF:mfidl.IMFVideoProcessorControl.SetSourceRectangle
title: IMFVideoProcessorControl::SetSourceRectangle
author: windows-sdk-content
description: Sets the source rectangle.
old-location: mf\imfvideoprocessorcontrol_setsourcerectangle.htm
tech.root: medfound
ms.assetid: 0A4E74BB-6F98-4610-9F47-5BD1E58B8589
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFVideoProcessorControl interface [Media Foundation],SetSourceRectangle method, IMFVideoProcessorControl.SetSourceRectangle, IMFVideoProcessorControl::SetSourceRectangle, SetSourceRectangle, SetSourceRectangle method [Media Foundation], SetSourceRectangle method [Media Foundation],IMFVideoProcessorControl interface, mf.imfvideoprocessorcontrol_setsourcerectangle, mfidl/IMFVideoProcessorControl::SetSourceRectangle
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
 - IMFVideoProcessorControl.SetSourceRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoProcessorControl::SetSourceRectangle


## -description


Sets the source rectangle. The source rectangle is the portion of the input frame that is blitted to the destination surface.


## -parameters




### -param pSrcRect

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the source rectangle.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



See <a href="https://msdn.microsoft.com/1476995A-9692-4B08-8EF7-7DB6321BEC24">Video Processor MFT</a> for info regarding source and destination rectangles in the <b>Video Processor MFT</b>.   




## -see-also




<a href="https://msdn.microsoft.com/6803B69E-CF84-45D5-804C-BD961BD5E13D">IMFVideoProcessorControl</a>
 

 

