---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.TransferVideoFrame
title: IMFMediaEngineProtectedContent::TransferVideoFrame method
author: windows-driver-content
description: Copies a protected video frame to a DXGI surface.
old-location: mf\imfmediaengineprotectedcontent_transfervideoframe.htm
old-project: medfound
ms.assetid: 3A5C6908-65F4-4E7A-AD71-BBD1C2A4ACE3
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMFMediaEngineProtectedContent, IMFMediaEngineProtectedContent interface [Media Foundation], TransferVideoFrame method, IMFMediaEngineProtectedContent::TransferVideoFrame, TransferVideoFrame method [Media Foundation], TransferVideoFrame method [Media Foundation], IMFMediaEngineProtectedContent interface, TransferVideoFrame,IMFMediaEngineProtectedContent.TransferVideoFrame, mf.imfmediaengineprotectedcontent_transfervideoframe, mfmediaengine/IMFMediaEngineProtectedContent::TransferVideoFrame
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineProtectedContent.TransferVideoFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineProtectedContent::TransferVideoFrame method


## -description


Copies a protected video frame to a DXGI surface.


## -parameters




### -param pDstSurf [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the destination surface.


### -param pSrc [in]

A pointer to an <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure that specifies the source rectangle.


### -param pDst [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the destination rectangle.


### -param pBorderClr [in]

A pointer to an <a href="https://msdn.microsoft.com/ce7ac174-9f00-42a4-9b48-ed86b406d83e">MFARGB</a> structure that specifies the border color. 


### -param pFrameProtectionFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/6864ED4B-BB75-4176-992B-ABC95B81001A">MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS</a> enumeration. These flags indicate which content protections the application must apply before presenting the surface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For protected content, call this method instead of the <a href="https://msdn.microsoft.com/07DB29E2-9F09-46CB-B138-197D95EC37F0">IMFMediaEngine::TransferVideoFrame</a> method.




## -see-also




<a href="https://msdn.microsoft.com/85B37711-DB46-4BC7-A051-79E9507791FA">IMFMediaEngineProtectedContent</a>
 

 

