---
UID: NN:msinkaut.IInkTablets
title: IInkTablets (msinkaut.h)
description: . (IInkTablets)
helpviewer_keywords: ["IInkTablets","IInkTablets interface [Tablet PC]","IInkTablets interface [Tablet PC]","described","msinkaut/IInkTablets","tablet.iinktablets"]
old-location: tablet\iinktablets.htm
tech.root: tablet
ms.assetid: 98052ECB-9385-45C9-A03C-3F312ADD9872
ms.date: 12/05/2018
ms.keywords: IInkTablets, IInkTablets interface [Tablet PC], IInkTablets interface [Tablet PC],described, msinkaut/IInkTablets, tablet.iinktablets
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
 - IInkTablets
 - msinkaut/IInkTablets
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
 - IInkTablets
---

# IInkTablets interface


## -description

Represents the object used to capture ink from available tablet devices.

## -inheritance

The <b>IInkTablets</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkTablets</b> also has these types of members:

## -remarks

Creating the InkCollector control behind a transparent control (such as a GroupBox with the WS_EX_TRANSPARENT property set) will prevent InkCollector from collecting ink.

## -see-also

[InkCollector class](/windows/win32/tablet/inkcollector-class)
