---
UID: NN:d2d1_1.ID2D1CommandSink
title: ID2D1CommandSink (d2d1_1.h)
description: The command sink is implemented by you for an application when you want to receive a playback of the commands recorded in a command list.
helpviewer_keywords: ["ID2D1CommandSink","ID2D1CommandSink interface [Direct2D]","ID2D1CommandSink interface [Direct2D]","described","d2d1_1/ID2D1CommandSink","direct2d.id2d1commandsink"]
old-location: direct2d\id2d1commandsink.htm
tech.root: Direct2D
ms.assetid: 4e0ce837-7f4e-4b93-8dd7-68f60cfb1105
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink, ID2D1CommandSink interface [Direct2D], ID2D1CommandSink interface [Direct2D],described, d2d1_1/ID2D1CommandSink, direct2d.id2d1commandsink
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1CommandSink
 - d2d1_1/ID2D1CommandSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1CommandSink
---

# ID2D1CommandSink interface


## -description

The command sink is implemented by you for an application when you want to receive a playback of the commands recorded in a command list. A typical usage will be for transforming the command list into another format such as XPS when some degree of conversion between the <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> primitives and the target format is required.



The command sink interface doesn't have any resource creation methods on it. The resources are still logically bound to the <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> device on which the command list was created and will be passed in to the command sink implementation.

## -inheritance

The <b>ID2D1CommandSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1CommandSink</b> also has these types of members:

## -remarks

The <b>ID2D1CommandSink</b> can be implemented to receive a play-back of the commands recorded in a command list. This interface is typically used for transforming the command list into another format  where some degree of conversion between the Direct2D primitives and the target format is required.
      
      

The <b>ID2D1CommandSink</b> interface does not have any resource creation methods. The resources are logically bound to the Direct2D device on which the <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a> was created and will be passed in to the <b>ID2D1CommandSink</b> implementation.
      
      

Not all methods implemented by <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a> are present.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
