---
UID: NN:richole.IRichEditOleCallback
title: IRichEditOleCallback (richole.h)
description: The IRichEditOleCallback interface is used by a rich text edit control to retrieve OLE-related information from its client.
helpviewer_keywords: ["IRichEditOleCallback","IRichEditOleCallback interface [Windows Controls]","IRichEditOleCallback interface [Windows Controls]","described","_win32_IRichEditOleCallback","_win32_IRichEditOleCallback_cpp","controls.IRichEditOleCallback","controls._win32_IRichEditOleCallback","richole/IRichEditOleCallback"]
old-location: controls\IRichEditOleCallback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback.htm
ms.date: 12/05/2018
ms.keywords: IRichEditOleCallback, IRichEditOleCallback interface [Windows Controls], IRichEditOleCallback interface [Windows Controls],described, _win32_IRichEditOleCallback, _win32_IRichEditOleCallback_cpp, controls.IRichEditOleCallback, controls._win32_IRichEditOleCallback, richole/IRichEditOleCallback
req.header: richole.h
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
 - IRichEditOleCallback
 - richole/IRichEditOleCallback
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
 - IRichEditOleCallback
---

# IRichEditOleCallback interface


## -description

The <b>IRichEditOleCallback</b> interface is used by a rich text edit control to retrieve OLE-related information from its client. A rich edit control client is responsible for implementing this interface and assigning it to the control by using the <a href="/windows/desktop/Controls/em-setolecallback">EM_SETOLECALLBACK</a> message.

## -inheritance

The <b>IRichEditOleCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRichEditOleCallback</b> also has these types of members:

