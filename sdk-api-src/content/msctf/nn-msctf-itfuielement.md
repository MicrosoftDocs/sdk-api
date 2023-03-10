---
UID: NN:msctf.ITfUIElement
title: ITfUIElement (msctf.h)
description: The ITfUIElement interface is a base interface of the UIElement object and is implemented by a text service.
helpviewer_keywords: ["ITfUIElement","ITfUIElement interface [Text Services Framework]","ITfUIElement interface [Text Services Framework]","described","_tsf_itfuielement_ref","msctf/ITfUIElement","tsf.itfuielement"]
old-location: tsf\itfuielement.htm
tech.root: TSF
ms.assetid: 651c3ca1-5e5b-4978-80d2-2183bd158610
ms.date: 12/05/2018
ms.keywords: ITfUIElement, ITfUIElement interface [Text Services Framework], ITfUIElement interface [Text Services Framework],described, _tsf_itfuielement_ref, msctf/ITfUIElement, tsf.itfuielement
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITfUIElement
 - msctf/ITfUIElement
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
 - ITfUIElement
---

# ITfUIElement interface


## -description

The <a href="/windows/desktop/api/msctf/nn-msctf-itfuielementsink">ITfUIElement</a> interface is a base interface of the UIElement object and is implemented by a text service.

## -inheritance

The <b>ITfUIElement</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfUIElement</b> also has these types of members:

## -remarks

A text service may implement some other UIElement interface such as <a href="/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielement">ITfCandidateListUIElement</a> in the same object that can be obtained by QI. A text service may implement only the <b>ITfUIElement</b> interface to a UI object that does not have to be drawn by the application but the show status can be controlled by the application. A text service that is categorized by GUID_TFCAT_TIPCAP_UIELEMENTENABLED needs to implement ITfUIElement for any UI object.
