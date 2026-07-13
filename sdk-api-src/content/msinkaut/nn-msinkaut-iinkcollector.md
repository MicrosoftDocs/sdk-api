---
UID: NN:msinkaut.IInkCollector
title: IInkCollector (msinkaut.h)
description: . (IInkCollector)
helpviewer_keywords: ["IInkCollector","IInkCollector interface [Tablet PC]","IInkCollector interface [Tablet PC]","described","msinkaut/IInkCollector","tablet.iinkcollector"]
old-location: tablet\iinkcollector.htm
tech.root: tablet
ms.assetid: 4E539E4F-2E7F-44ED-A8D0-650BCAFDFAFB
ms.date: 12/05/2018
ms.keywords: IInkCollector, IInkCollector interface [Tablet PC], IInkCollector interface [Tablet PC],described, msinkaut/IInkCollector, tablet.iinkcollector
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
 - IInkCollector
 - msinkaut/IInkCollector
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
 - IInkCollector
---

# IInkCollector interface


## -description

Represents the object used to capture ink from available tablet devices.

## -inheritance

The <b>IInkCollector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. 

## -remarks

Creating the InkCollector control behind a transparent control (such as a GroupBox with the WS_EX_TRANSPARENT property set) will prevent InkCollector from collecting ink.

## -see-also

[InkCollector class](/windows/win32/tablet/inkcollector-class)
