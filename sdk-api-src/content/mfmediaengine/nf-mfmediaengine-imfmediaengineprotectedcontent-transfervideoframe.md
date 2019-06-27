---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.TransferVideoFrame
title: IMFMediaEngineProtectedContent::TransferVideoFrame (mfmediaengine.h)
author: windows-sdk-content
description: Copies a protected video frame to a DXGI surface.
old-location: mf\imfmediaengineprotectedcontent_transfervideoframe.htm
tech.root: medfound
ms.assetid: 3A5C6908-65F4-4E7A-AD71-BBD1C2A4ACE3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineProtectedContent interface [Media Foundation],TransferVideoFrame method, IMFMediaEngineProtectedContent.TransferVideoFrame, IMFMediaEngineProtectedContent::TransferVideoFrame, TransferVideoFrame, TransferVideoFrame method [Media Foundation], TransferVideoFrame method [Media Foundation],IMFMediaEngineProtectedContent interface, mf.imfmediaengineprotectedcontent_transfervideoframe, mfmediaengine/IMFMediaEngineProtectedContent::TransferVideoFrame
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineProtectedContent.TransferVideoFrame"
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineProtectedContent.TransferVideoFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineProtectedContent::TransferVideoFrame


## -description


Copies a protected video frame to a DXGI surface.


## -parameters




### -param pDstSurf [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the destination surface.


### -param pSrc [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect">MFVideoNormalizedRect</a> structure that specifies the source rectangle.


### -param pDst [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the destination rectangle.


### -param pBorderClr [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-_mfargb">MFARGB</a> structure that specifies the border color. 


### -param pFrameProtectionFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_frame_protection_flags">MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS</a> enumeration. These flags indicate which content protections the application must apply before presenting the surface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For protected content, call this method instead of the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-transfervideoframe">IMFMediaEngine::TransferVideoFrame</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent">IMFMediaEngineProtectedContent</a>
 

 

