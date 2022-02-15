---
UID: NN:control.IQueueCommand
title: IQueueCommand (control.h)
description: The IQueueCommand interface queues a command for processing at a designated time.
helpviewer_keywords: ["IQueueCommand","IQueueCommand interface [DirectShow]","IQueueCommand interface [DirectShow]","described","IQueueCommandInterface","control/IQueueCommand","dshow.iqueuecommand"]
old-location: dshow\iqueuecommand.htm
tech.root: dshow
ms.assetid: 08efcbec-ce17-44e8-a3c1-4b5b95dcaaa4
ms.date: 12/05/2018
ms.keywords: IQueueCommand, IQueueCommand interface [DirectShow], IQueueCommand interface [DirectShow],described, IQueueCommandInterface, control/IQueueCommand, dshow.iqueuecommand
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueueCommand
 - control/IQueueCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IQueueCommand
---

# IQueueCommand interface


## -description

The <code>IQueueCommand</code> interface queues a command for processing at a designated time. The Filter Graph Manager exposes this interface. Applications can use it to queue graph-control commands in advance.

The methods in <code>IQueueCommand</code> are modeled after the <b>IDispatch::InvokeAt</b> method. The application specifies an interface, a method on the interface, parameters to the method, and a reference time. The Filter Graph Manager queues this information and then invokes the method at the specified time. The requested interface must inherit <b>IDispatch</b> and must be exposed by the Filter Graph Manager. Examples include <a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl</a>, <a href="/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx</a>, and <a href="/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition</a>.

When the command is queued, the filter graph manager returns a pointer to the <a href="/windows/desktop/api/control/nn-control-ideferredcommand">IDeferredCommand</a> interface. The application can use this interface to cancel or modify the command.

<div class="alert"><b>Note</b>  The two methods in <code>IQueueCommand</code> refer to stream time and presentation time, respectively. In the context of the Filter Graph Manager, stream time and presentation time are identical, so there is no functional difference between the two methods. Other objects could implement <code>IQueueCommand</code> differently. For more information about stream time and presentation time, see <a href="/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.</div>
<div> </div>

## -inheritance

The <b>IQueueCommand</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueueCommand</b> also has these types of members:

