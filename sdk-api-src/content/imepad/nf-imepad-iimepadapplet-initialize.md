---
UID: NF:imepad.IImePadApplet.Initialize
title: IImePadApplet::Initialize (imepad.h)
description: Called from IImePad interface to initialize IImePadApplet.
helpviewer_keywords: ["IImePadApplet interface [Internationalization for Windows Applications]","Initialize method","IImePadApplet.Initialize","IImePadApplet::Initialize","Initialize","Initialize method [Internationalization for Windows Applications]","Initialize method [Internationalization for Windows Applications]","IImePadApplet interface","imepad/IImePadApplet::Initialize","intl.iimepadapplet_initialize"]
old-location: intl\iimepadapplet_initialize.htm
tech.root: Intl
ms.assetid: E76FF3FC-717F-42B8-AC5E-45D5527882A7
ms.date: 12/05/2018
ms.keywords: IImePadApplet interface [Internationalization for Windows Applications],Initialize method, IImePadApplet.Initialize, IImePadApplet::Initialize, Initialize, Initialize method [Internationalization for Windows Applications], Initialize method [Internationalization for Windows Applications],IImePadApplet interface, imepad/IImePadApplet::Initialize, intl.iimepadapplet_initialize
req.header: imepad.h
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
 - IImePadApplet::Initialize
 - imepad/IImePadApplet::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imepad.h
api_name:
 - IImePadApplet.Initialize
---

# IImePadApplet::Initialize


## -description

Called from <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> interface to initialize <a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a>.

## -parameters

### -param lpIImePad

Pointer to <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> (<b>IUnknown</b> *)

## -returns

<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.

## -remarks

When the ImePad user interface is created, <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> calls this method and sets the IImePad interface pointer as an argument. The applet can save and use this pointer to call the <a href="/windows/desktop/api/imepad/nf-imepad-iimepad-request">pIImePad->IImePad::Request</a> method.

## -see-also

<a href="/windows/desktop/api/imepad/nn-imepad-iimepadapplet">IImePadApplet</a>