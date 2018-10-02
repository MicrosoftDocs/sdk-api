---
UID: NF:inkpresenterdesktop.IInkDesktopHost.QueueWorkItem
title: IInkDesktopHost::QueueWorkItem
author: windows-sdk-content
description: Add an ink operation to a work queue for execution on the IInkDesktopHost thread.
old-location: input_ink\iinkdesktophost_queueworkitem.htm
tech.root: input_ink
ms.assetid: c8c5e1c4-c5a5-4172-a101-66276b7024e2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IInkDesktopHost interface,QueueWorkItem method, IInkDesktopHost.QueueWorkItem, IInkDesktopHost::QueueWorkItem, InkPresenterDesktop.iinkdesktophost_queueworkitem, QueueWorkItem, QueueWorkItem method, QueueWorkItem method,IInkDesktopHost interface, inkpresenterdesktop/IInkDesktopHost::QueueWorkItem, input_ink.iinkdesktophost_queueworkitem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDesktopHost::QueueWorkItem


## -description


Add an ink operation to a work queue for execution on the <a href="https://msdn.microsoft.com/7a577536-405b-400d-89bc-c3b3894b448d">IInkDesktopHost</a> thread.

The app is responsible for synchronizing the work queue with the UI thread.


## -parameters




### -param workItem [in]

An <a href="https://msdn.microsoft.com/812026bf-74d0-49c2-851c-de64a6417bff">IInkHostWorkItem</a> object representing an ink operation.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=620314">Complex ink sample</a>



<a href="https://msdn.microsoft.com/7a577536-405b-400d-89bc-c3b3894b448d">IInkDesktopHost</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620308">Ink sample</a>



<a href="https://msdn.microsoft.com/3DA4F2D2-5405-42A1-9ED9-3A87BCD84C43">Pen and stylus interactions</a>



<b>Samples</b>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620312">Simple ink sample</a>
 

 

