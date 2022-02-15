---
UID: NL:textserv.ITextServices
title: ITextServices (textserv.h)
description: Extends the Text Object Model (TOM) to provide extra functionality for windowless operation.
helpviewer_keywords: ["ITextServices","ITextServices interface [Windows Controls]","ITextServices interface [Windows Controls]","described","_win32_ITextServices","_win32_ITextServices_cpp","controls.ITextServices","controls._win32_ITextServices","textserv/ITextServices"]
old-location: controls\ITextServices.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itextservices.htm
ms.date: 12/05/2018
ms.keywords: ITextServices, ITextServices interface [Windows Controls], ITextServices interface [Windows Controls],described, _win32_ITextServices, _win32_ITextServices_cpp, controls.ITextServices, controls._win32_ITextServices, textserv/ITextServices
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextServices
 - textserv/ITextServices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextServices
---

# ITextServices class


## -description

Extends the Text Object Model (TOM) to provide extra functionality for windowless operation.

## -inheritance

The <b>ITextServices</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextServices</b> also has these types of members:

## -remarks

In conjunction with the <a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a> interface, <b>ITextServices</b> provides the means by which a rich edit control can be used <i>without</i> creating a window.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Applications do not implement the <b>ITextServices</b> interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications can call the <a href="/windows/desktop/api/textserv/nf-textserv-createtextservices">CreateTextServices</a> function to create a text services object. To retrieve an <b>ITextServices</b> pointer, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the private <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer returned by <b>CreateTextServices</b>. You can then call the <b>ITextServices</b> methods to send messages to the text services object.

## -see-also

<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>
