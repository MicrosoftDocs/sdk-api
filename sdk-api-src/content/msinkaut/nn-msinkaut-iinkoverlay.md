---
UID: NN:msinkaut.IInkOverlay
title: IInkOverlay (msinkaut.h)
description: . (IInkOverlay)
helpviewer_keywords: ["IInkOverlay","IInkOverlay interface [Tablet PC]","IInkOverlay interface [Tablet PC]","described","msinkaut/IInkOverlay","tablet.iinkoverlay"]
old-location: tablet\iinkoverlay.htm
tech.root: tablet
ms.assetid: ACE11946-113B-42EE-A3F1-0036B1DF8141
ms.date: 12/05/2018
ms.keywords: IInkOverlay, IInkOverlay interface [Tablet PC], IInkOverlay interface [Tablet PC],described, msinkaut/IInkOverlay, tablet.iinkoverlay
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkOverlay
 - msinkaut/IInkOverlay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkOverlay
---

# IInkOverlay interface


## -description

Represents an object that is useful for annotation scenarios where users are not concerned with performing recognition on ink but instead are interested in the size, shape, color, and position of the ink.

## -inheritance

The <b>IInkOverlay</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. 

## -remarks

Creating the InkOverlay control behind a transparent control (such as a GroupBox with the WS_EX_TRANSPARENT property set) will prevent InkOverlay from collecting ink.

## -see-also

[IInkCollector interface](nn-msinkaut-iinkcollector.md), [IInkOverlay interface](nn-msinkaut-iinkoverlay.md), [InkOverlay class](/windows/win32/tablet/inkoverlay-class)
