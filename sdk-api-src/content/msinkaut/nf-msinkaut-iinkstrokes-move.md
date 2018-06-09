---
UID: NF:msinkaut.IInkStrokes.Move
title: IInkStrokes::Move
author: windows-sdk-content
description: Applies a translation to the ink of an IInkStrokeDisp object or InkStrokes collection.
old-location: tablet\inkstrokes_move.htm
old-project: tablet
ms.assetid: 4754a211-b90c-453a-91b2-9f49ad31621d
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 2d3425c0-6000-4478-9c67-5fdb8e2316e5, IInkStrokes interface [Tablet PC],Move method, IInkStrokes.Move, IInkStrokes::Move, Move, Move method [Tablet PC], Move method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::Move, tablet.inkstrokes_move
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
 - IInkStrokes.Move
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkStrokes::Move


## -description



Applies a translation to the ink of an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object or <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.




## -parameters




### -param HorizontalComponent [in]

The distance in ink space coordinates to translate the view transform in the X dimension.


### -param VerticalComponent [in]

The distance in ink space coordinates to translate the view transform in the Y dimension.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="tablet.iinkstrokes">IInkStrokes</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

