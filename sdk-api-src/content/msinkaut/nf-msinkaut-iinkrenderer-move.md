---
UID: NF:msinkaut.IInkRenderer.Move
title: IInkRenderer::Move
author: windows-sdk-content
description: Applies a translation to the view transform in ink space coordinates.
old-location: tablet\inkrenderer_move.htm
old-project: tablet
ms.assetid: a5cba79f-2ae8-43ed-bef5-1ec86da9470a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IInkRenderer, IInkRenderer interface [Tablet PC],Move method, IInkRenderer.Move, IInkRenderer::Move, Move, Move method [Tablet PC], Move method [Tablet PC],IInkRenderer interface, a5cba79f-2ae8-43ed-bef5-1ec86da9470a, msinkaut/IInkRenderer::Move, tablet.inkrenderer_move
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRenderer::Move


## -description



Applies a translation to the <a href="https://msdn.microsoft.com/8a4d768d-09b6-45e1-b412-e267d92cc3ef">view transform</a> in ink space coordinates.




## -parameters




### -param HorizontalComponent [in]

The amount in ink space coordinates to translate the view transform in the X dimension.


### -param VerticalComponent [in]

The amount in ink space coordinates to translate the view transform in the Y dimension.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846805(v=VS.85).aspx">IInkRenderer</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>
 

 

