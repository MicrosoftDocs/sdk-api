---
UID: NF:faxcomex.IFaxIncomingQueue.put_Blocked
title: IFaxIncomingQueue::put_Blocked (faxcomex.h)
description: The Blocked property is a Boolean value that indicates whether the job queue for incoming faxes is blocked. (Put)
helpviewer_keywords: ["Blocked property [Fax Service]","Blocked property [Fax Service]","IFaxIncomingQueue interface","IFaxIncomingQueue interface [Fax Service]","Blocked property","IFaxIncomingQueue.Blocked","IFaxIncomingQueue.put_Blocked","IFaxIncomingQueue::Blocked","IFaxIncomingQueue::get_Blocked","IFaxIncomingQueue::put_Blocked","_mfax_faxincomingqueue.blocked","fax._mfax_faxincomingqueue_blocked","fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_blocked_cpp","faxcomex/IFaxIncomingQueue::Blocked","faxcomex/IFaxIncomingQueue::get_Blocked","faxcomex/IFaxIncomingQueue::put_Blocked","put_Blocked"]
old-location: fax\_mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_blocked_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2rac.htm
ms.date: 12/05/2018
ms.keywords: Blocked property [Fax Service], Blocked property [Fax Service],IFaxIncomingQueue interface, IFaxIncomingQueue interface [Fax Service],Blocked property, IFaxIncomingQueue.Blocked, IFaxIncomingQueue.put_Blocked, IFaxIncomingQueue::Blocked, IFaxIncomingQueue::get_Blocked, IFaxIncomingQueue::put_Blocked, _mfax_faxincomingqueue.blocked, fax._mfax_faxincomingqueue_blocked, fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_blocked_cpp, faxcomex/IFaxIncomingQueue::Blocked, faxcomex/IFaxIncomingQueue::get_Blocked, faxcomex/IFaxIncomingQueue::put_Blocked, put_Blocked
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxIncomingQueue::put_Blocked
 - faxcomex/IFaxIncomingQueue::put_Blocked
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxIncomingQueue.Blocked
 - IFaxIncomingQueue.get_Blocked
 - IFaxIncomingQueue.put_Blocked
---

# IFaxIncomingQueue::put_Blocked


## -description

The <b>Blocked</b> property is a Boolean value that indicates whether the job queue for incoming faxes is blocked. 

This property is read/write.

## -parameters

## -remarks

If this property is equal to <b>TRUE</b>, the inbound job queue is blocked and the fax service is not answering incoming fax calls. If this property is equal to <b>FALSE</b>, the queue is not blocked.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingqueue">FaxIncomingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingqueue">IFaxIncomingQueue</a>
