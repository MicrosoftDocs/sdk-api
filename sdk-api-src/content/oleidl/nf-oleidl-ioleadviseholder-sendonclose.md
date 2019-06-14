---
UID: NF:oleidl.IOleAdviseHolder.SendOnClose
title: IOleAdviseHolder::SendOnClose (oleidl.h)
author: windows-sdk-content
description: Sends notification to all advisory sinks currently registered with the advise holder that the object has closed.
old-location: com\ioleadviseholder_sendonclose.htm
tech.root: com
ms.assetid: f4efa947-d357-432c-9585-b00b19551ad6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOleAdviseHolder interface [COM],SendOnClose method, IOleAdviseHolder.SendOnClose, IOleAdviseHolder::SendOnClose, SendOnClose, SendOnClose method [COM], SendOnClose method [COM],IOleAdviseHolder interface, _ole_ioleadviseholder_sendonclose, com.ioleadviseholder_sendonclose, oleidl/IOleAdviseHolder::SendOnClose
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - OleIdl.h
api_name:
 - IOleAdviseHolder.SendOnClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleAdviseHolder::SendOnClose


## -description


Sends notification to all advisory sinks currently registered with the advise holder that the object has closed.


## -parameters






## -returns



This method returns S_OK if advise sinks were notified of the close operation through a call to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iadvisesink-onclose">IAdviseSink::OnClose</a> method.




## -remarks



<b>SendOnClose</b> must call <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iadvisesink-onclose">IAdviseSink::OnClose</a> on all advise sinks that have a valid advisory connection with the object, whenever the object goes from the running state to the loaded state. This occurs through a call to <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>, so you can call <b>SendOnClose</b> when you determine that a Close operation has been successful.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iadvisesink-onclose">IAdviseSink::OnClose</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a>
 

 

