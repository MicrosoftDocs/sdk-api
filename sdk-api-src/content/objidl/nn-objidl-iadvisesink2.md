---
UID: NN:objidl.IAdviseSink2
title: IAdviseSink2 (objidl.h)
description: The IAdviseSink2 interface is an extension of the IAdviseSink interface, adding the method OnLinkSrcChange to the contract to handle a change in the moniker of a linked object.
helpviewer_keywords: ["IAdviseSink2","IAdviseSink2 interface [COM]","IAdviseSink2 interface [COM]","described","_ole_iadvisesink2","com.iadvisesink2","objidl/IAdviseSink2"]
old-location: com\iadvisesink2.htm
tech.root: com
ms.assetid: 80f55377-8a1e-42b1-8fe0-5896620c8062
ms.date: 12/05/2018
ms.keywords: IAdviseSink2, IAdviseSink2 interface [COM], IAdviseSink2 interface [COM],described, _ole_iadvisesink2, com.iadvisesink2, objidl/IAdviseSink2
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
 - IAdviseSink2
 - objidl/IAdviseSink2
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
 - IAdviseSink2
---

# IAdviseSink2 interface


## -description

The <b>IAdviseSink2</b> interface is an extension of the <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface, adding the method <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink2-onlinksrcchange">OnLinkSrcChange</a> to the contract to handle a change in the moniker of a linked object. This avoids overloading the implementation <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onrename">IAdviseSink::OnRename</a> to handle the renaming of both embedded objects and linked objects. In applications where different blocks of code might execute depending on which of these two similar events has occurred, using the same method for both events complicates testing and debugging.

## -inheritance

The <b>IAdviseSink2</b> interface inherits from <b>IAdviseSink</b>. <b>IAdviseSink2</b> also has these types of members:

