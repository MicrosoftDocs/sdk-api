---
UID: NF:inkpresenterdesktop.IInkDesktopHost.QueueWorkItem
title: IInkDesktopHost::QueueWorkItem (inkpresenterdesktop.h)
description: Add an ink operation to a work queue for execution on the IInkDesktopHost thread.
old-location: input_ink\iinkdesktophost_queueworkitem.htm
tech.root: input_ink
ms.assetid: c8c5e1c4-c5a5-4172-a101-66276b7024e2
ms.date: 12/05/2018
ms.keywords: IInkDesktopHost interface,QueueWorkItem method, IInkDesktopHost.QueueWorkItem, IInkDesktopHost::QueueWorkItem, InkPresenterDesktop.iinkdesktophost_queueworkitem, QueueWorkItem, QueueWorkItem method, QueueWorkItem method,IInkDesktopHost interface, inkpresenterdesktop/IInkDesktopHost::QueueWorkItem, input_ink.iinkdesktophost_queueworkitem
ms.topic: method
f1_keywords:
- inkpresenterdesktop/IInkDesktopHost.QueueWorkItem
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkPresenterDesktop.h
api_name:
- IInkDesktopHost.QueueWorkItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDesktopHost::QueueWorkItem


## -description


Add an ink operation to a work queue for execution on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost">IInkDesktopHost</a> thread.

The app is responsible for synchronizing the work queue with the UI thread.


## -parameters




### -param workItem [in]

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem">IInkHostWorkItem</a> object representing an ink operation.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=620314">Complex ink sample</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost">IInkDesktopHost</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620308">Ink sample</a>



<a href="https://docs.microsoft.com/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>



<b>Samples</b>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620312">Simple ink sample</a>
 

 

