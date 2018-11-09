---
UID: NF:mfmediaengine.IMFMediaEngine.TransferVideoFrame
title: IMFMediaEngine::TransferVideoFrame
author: windows-sdk-content
description: Copies the current video frame to a DXGI surface or WIC bitmap.
old-location: mf\imfmediaengine_transfervideoframe.htm
tech.root: medfound
ms.assetid: 07DB29E2-9F09-46CB-B138-197D95EC37F0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],TransferVideoFrame method, IMFMediaEngine.TransferVideoFrame, IMFMediaEngine::TransferVideoFrame, TransferVideoFrame, TransferVideoFrame method [Media Foundation], TransferVideoFrame method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_transfervideoframe, mfmediaengine/IMFMediaEngine::TransferVideoFrame
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
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
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.TransferVideoFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngine::TransferVideoFrame


## -description


Copies the current video frame to a DXGI surface or WIC bitmap.


## -parameters




### -param pDstSurf [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the destination surface. 


### -param pSrc [in]

A pointer to an <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure that specifies the source rectangle.


### -param pDst [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the destination rectangle.


### -param pBorderClr [in]

A pointer to an <a href="https://msdn.microsoft.com/ce7ac174-9f00-42a4-9b48-ed86b406d83e">MFARGB</a> structure that specifies the border color. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In frame-server mode, call this method to blit the video frame to a DXGI or WIC surface. The application can call this method at any time after the Media Engine loads a video resource. Typically, however, the application calls <a href="https://msdn.microsoft.com/EC06D3D6-F103-4932-96C1-B55A59CD5E34">IMFMediaEngine::OnVideoStreamTick</a> first, to determine whether a new frame is available. If <b>OnVideoStreamTick</b> returns <b>S_OK</b>, the application then calls <b>TransferVideoFrame</b>.

The Media Engine scales and letterboxes the video to fit the destination rectangle. It fills the letterbox area with the border color.

For protected content, call the <a href="https://msdn.microsoft.com/3A5C6908-65F4-4E7A-AD71-BBD1C2A4ACE3">IMFMediaEngineProtectedContent::TransferVideoFrame</a> method instead of this method.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

