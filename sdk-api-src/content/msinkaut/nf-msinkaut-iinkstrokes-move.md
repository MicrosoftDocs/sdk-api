---
UID: NF:msinkaut.IInkStrokes.Move
title: IInkStrokes::Move (msinkaut.h)
description: Applies a translation to the ink of an IInkStrokeDisp object or InkStrokes collection.
helpviewer_keywords: ["2d3425c0-6000-4478-9c67-5fdb8e2316e5","IInkStrokes interface [Tablet PC]","Move method","IInkStrokes.Move","IInkStrokes::Move","Move","Move method [Tablet PC]","Move method [Tablet PC]","IInkStrokes interface","msinkaut/IInkStrokes::Move","tablet.inkstrokes_move"]
old-location: tablet\inkstrokes_move.htm
tech.root: tablet
ms.assetid: 4754a211-b90c-453a-91b2-9f49ad31621d
ms.date: 12/05/2018
ms.keywords: 2d3425c0-6000-4478-9c67-5fdb8e2316e5, IInkStrokes interface [Tablet PC],Move method, IInkStrokes.Move, IInkStrokes::Move, Move, Move method [Tablet PC], Move method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::Move, tablet.inkstrokes_move
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkStrokes::Move
 - msinkaut/IInkStrokes::Move
dev_langs:
 - c++
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
---

# IInkStrokes::Move


## -description

Applies a translation to the ink of an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object or <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

## -parameters

### -param HorizontalComponent [in]

The distance in ink space coordinates to translate the view transform in the X dimension.

### -param VerticalComponent [in]

The distance in ink space coordinates to translate the view transform in the Y dimension.

## -returns

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/Mt846806(v=VS.85).aspx">IInkStrokes</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>