---
UID: NN:callobj.ICallUnmarshal
title: ICallUnmarshal (callobj.h)
description: Is used on the server (receiving) side of a remote invocation.
helpviewer_keywords: ["ICallUnmarshal","ICallUnmarshal interface [COM]","ICallUnmarshal interface [COM]","described","_com_icallunmarshal_interface","callobj/ICallUnmarshal","com.icallunmarshal"]
old-location: com\icallunmarshal.htm
tech.root: com
ms.assetid: 66de8d71-c27c-41bd-a741-02de5c779290
ms.date: 12/05/2018
ms.keywords: ICallUnmarshal, ICallUnmarshal interface [COM], ICallUnmarshal interface [COM],described, _com_icallunmarshal_interface, callobj/ICallUnmarshal, com.icallunmarshal
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
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
 - ICallUnmarshal
 - callobj/ICallUnmarshal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallUnmarshal
---

# ICallUnmarshal interface


## -description

Is used on the server (receiving) side of a remote invocation. An appropriate instance of <b>ICallUnmarshal</b> can be used to transform back into a call frame a method invocation previously marshaled by a call to <a href="/windows/desktop/api/callobj/nf-callobj-icallframe-marshal">ICallFrame::Marshal</a> on the client (sending) side. After such a reconstituted call frame is obtained, the call can be carried out on an actual object using <a href="/windows/desktop/api/callobj/nf-callobj-icallframe-invoke">ICallFrame::Invoke</a>.

## -inheritance

The <b>ICallUnmarshal</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICallUnmarshal</b> also has these types of members:

