---
UID: NF:msinkaut.IInkRenderer.Move
title: IInkRenderer::Move (msinkaut.h)
description: Applies a translation to the view transform in ink space coordinates.helpviewer_keywords: ["IInkRenderer","IInkRenderer interface [Tablet PC]","Move method","IInkRenderer.Move","IInkRenderer::Move","Move","Move method [Tablet PC]","Move method [Tablet PC]","IInkRenderer interface","a5cba79f-2ae8-43ed-bef5-1ec86da9470a","msinkaut/IInkRenderer::Move","tablet.inkrenderer_move"]
old-location: tablet\inkrenderer_move.htm
tech.root: tablet
ms.assetid: a5cba79f-2ae8-43ed-bef5-1ec86da9470a
ms.date: 12/05/2018
ms.keywords: IInkRenderer, IInkRenderer interface [Tablet PC],Move method, IInkRenderer.Move, IInkRenderer::Move, Move, Move method [Tablet PC], Move method [Tablet PC],IInkRenderer interface, a5cba79f-2ae8-43ed-bef5-1ec86da9470a, msinkaut/IInkRenderer::Move, tablet.inkrenderer_move
f1_keywords:
- msinkaut/IInkRenderer.Move
dev_langs:
- c++
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkRenderer.Move
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRenderer::Move


## -description



Applies a translation to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform">view transform</a> in ink space coordinates.




## -parameters




### -param HorizontalComponent [in]

The amount in ink space coordinates to translate the view transform in the X dimension.


### -param VerticalComponent [in]

The amount in ink space coordinates to translate the view transform in the Y dimension.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846805(v=VS.85).aspx">IInkRenderer</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>
 

 

