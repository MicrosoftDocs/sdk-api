---
UID: NL:textserv.ITextHost
title: ITextHost (textserv.h)
description: The ITextHost interface is used by a text services object to obtain text host services.
helpviewer_keywords: ["ITextHost","ITextHost interface [Windows Controls]","ITextHost interface [Windows Controls]","described","_win32_ITextHost","_win32_ITextHost_cpp","controls.ITextHost","controls._win32_ITextHost","textserv/ITextHost"]
old-location: controls\ITextHost.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost.htm
ms.date: 12/05/2018
ms.keywords: ITextHost, ITextHost interface [Windows Controls], ITextHost interface [Windows Controls],described, _win32_ITextHost, _win32_ITextHost_cpp, controls.ITextHost, controls._win32_ITextHost, textserv/ITextHost
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
 - ITextHost
 - textserv/ITextHost
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
 - ITextHost
---

# ITextHost class


## -description

The <b>ITextHost</b> interface is used by a text services object to obtain text host services.

## -inheritance

The <b>ITextHost</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextHost</b> also has these types of members:

## -remarks

You must implement the <b>ITextHost</b> interface before you call the <a href="/windows/desktop/api/textserv/nf-textserv-createtextservices">CreateTextServices</a> function.

Applications do not call the <b>ITextHost</b> methods. A text services object created by the <a href="/windows/desktop/api/textserv/nf-textserv-createtextservices">CreateTextServices</a> function calls the interface methods.

## -see-also

<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>
