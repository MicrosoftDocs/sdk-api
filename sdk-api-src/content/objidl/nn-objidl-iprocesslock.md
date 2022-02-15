---
UID: NN:objidl.IProcessLock
title: IProcessLock (objidl.h)
description: Used by ISurrogateService to prevent the process from terminating due to a time-out.
helpviewer_keywords: ["IProcessLock","IProcessLock interface [COM]","IProcessLock interface [COM]","described","_com_iprocesslock","com.iprocesslock","objidl/IProcessLock"]
old-location: com\iprocesslock.htm
tech.root: com
ms.assetid: 49ec5657-d54e-4af7-8c20-00de383ecf89
ms.date: 12/05/2018
ms.keywords: IProcessLock, IProcessLock interface [COM], IProcessLock interface [COM],described, _com_iprocesslock, com.iprocesslock, objidl/IProcessLock
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IProcessLock
 - objidl/IProcessLock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IProcessLock
---

# IProcessLock interface


## -description

<p class="CCE_Message">[The use of this interface is not recommended; use the <a href="/windows/desktop/api/objidl/nn-objidl-iprocessinitcontrol">IProcessInitControl</a> interface instead.]

Used by <a href="/windows/desktop/api/objidl/nn-objidl-isurrogateservice">ISurrogateService</a> to prevent the process from terminating due to a time-out.

## -inheritance

The <b>IProcessLock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProcessLock</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iprocessinitcontrol">IProcessInitControl</a>
