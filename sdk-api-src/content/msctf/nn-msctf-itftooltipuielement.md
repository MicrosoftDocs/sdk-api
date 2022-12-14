---
UID: NN:msctf.ITfToolTipUIElement
title: ITfToolTipUIElement (msctf.h)
description: The ITfToolTipUIElement interface is implemented by a text service that wants to show a tooltip on its UI.
helpviewer_keywords: ["ITfToolTipUIElement","ITfToolTipUIElement interface [Text Services Framework]","ITfToolTipUIElement interface [Text Services Framework]","described","_tsf_itftooltipuielement_ref","msctf/ITfToolTipUIElement","tsf.itftooltipuielement"]
old-location: tsf\itftooltipuielement.htm
tech.root: TSF
ms.assetid: c881b251-a3fb-4f80-b2e8-08db1754f8f5
ms.date: 12/05/2018
ms.keywords: ITfToolTipUIElement, ITfToolTipUIElement interface [Text Services Framework], ITfToolTipUIElement interface [Text Services Framework],described, _tsf_itftooltipuielement_ref, msctf/ITfToolTipUIElement, tsf.itftooltipuielement
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfToolTipUIElement
 - msctf/ITfToolTipUIElement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfToolTipUIElement
---

# ITfToolTipUIElement interface


## -description

The <b>ITfToolTipUIElement</b> interface is implemented by a text service that wants to show a tooltip on its UI. A fullscreen application which wants to draw all UI by itself may want to draw the tooltip also or it can just hide the tooltip or of course it can let the text service show it. However, it does not guarantee that a text service can show the tooltip correctly when other UI are asked to be hidden.

## -inheritance

The <b>ITfToolTipUIElement</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfToolTipUIElement</b> also has these types of members:

