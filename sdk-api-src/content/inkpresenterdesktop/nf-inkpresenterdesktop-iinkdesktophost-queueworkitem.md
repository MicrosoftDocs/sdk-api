---
UID: NF:inkpresenterdesktop.IInkDesktopHost.QueueWorkItem
title: IInkDesktopHost::QueueWorkItem (inkpresenterdesktop.h)
description: Add an ink operation to a work queue for execution on the IInkDesktopHost thread.
helpviewer_keywords: ["IInkDesktopHost interface","QueueWorkItem method","IInkDesktopHost.QueueWorkItem","IInkDesktopHost::QueueWorkItem","InkPresenterDesktop.iinkdesktophost_queueworkitem","QueueWorkItem","QueueWorkItem method","QueueWorkItem method","IInkDesktopHost interface","inkpresenterdesktop/IInkDesktopHost::QueueWorkItem","input_ink.iinkdesktophost_queueworkitem"]
old-location: input_ink\iinkdesktophost_queueworkitem.htm
tech.root: input_ink
ms.assetid: c8c5e1c4-c5a5-4172-a101-66276b7024e2
ms.date: 12/05/2018
ms.keywords: IInkDesktopHost interface,QueueWorkItem method, IInkDesktopHost.QueueWorkItem, IInkDesktopHost::QueueWorkItem, InkPresenterDesktop.iinkdesktophost_queueworkitem, QueueWorkItem, QueueWorkItem method, QueueWorkItem method,IInkDesktopHost interface, inkpresenterdesktop/IInkDesktopHost::QueueWorkItem, input_ink.iinkdesktophost_queueworkitem
req.header: inkpresenterdesktop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InkPresenterDesktop.idl
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
 - IInkDesktopHost::QueueWorkItem
 - inkpresenterdesktop/IInkDesktopHost::QueueWorkItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkPresenterDesktop.h
api_name:
 - IInkDesktopHost.QueueWorkItem
---

# IInkDesktopHost::QueueWorkItem


## -description

Add an ink operation to a work queue for execution on the <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost">IInkDesktopHost</a> thread.

The app is responsible for synchronizing the work queue with the UI thread.

## -parameters

### -param workItem [in]

An <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem">IInkHostWorkItem</a> object representing an ink operation.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex ink sample</a>



<a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost">IInkDesktopHost</a>






<a href="/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>



<b>Samples</b>

<a href="https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex Ink sample</a>

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk">Simple ink sample</a>