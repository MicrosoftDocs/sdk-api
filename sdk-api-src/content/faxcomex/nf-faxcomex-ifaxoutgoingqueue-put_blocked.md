---
UID: NF:faxcomex.IFaxOutgoingQueue.put_Blocked
title: IFaxOutgoingQueue::put_Blocked (faxcomex.h)
description: The IFaxOutgoingQueue::get_Blocked property is a Boolean value that indicates whether the job queue for outgoing faxes is blocked. (Put)
helpviewer_keywords: ["Blocked property [Fax Service]","Blocked property [Fax Service]","IFaxOutgoingQueue interface","IFaxOutgoingQueue interface [Fax Service]","Blocked property","IFaxOutgoingQueue.Blocked","IFaxOutgoingQueue.put_Blocked","IFaxOutgoingQueue::Blocked","IFaxOutgoingQueue::get_Blocked","IFaxOutgoingQueue::put_Blocked","_mfax_faxoutgoingqueue.blocked","fax._mfax_faxoutgoingqueue_blocked","fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_blocked_cpp","faxcomex/IFaxOutgoingQueue::Blocked","faxcomex/IFaxOutgoingQueue::get_Blocked","faxcomex/IFaxOutgoingQueue::put_Blocked","put_Blocked"]
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_blocked_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_59d0.htm
ms.date: 12/05/2018
ms.keywords: Blocked property [Fax Service], Blocked property [Fax Service],IFaxOutgoingQueue interface, IFaxOutgoingQueue interface [Fax Service],Blocked property, IFaxOutgoingQueue.Blocked, IFaxOutgoingQueue.put_Blocked, IFaxOutgoingQueue::Blocked, IFaxOutgoingQueue::get_Blocked, IFaxOutgoingQueue::put_Blocked, _mfax_faxoutgoingqueue.blocked, fax._mfax_faxoutgoingqueue_blocked, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_blocked_cpp, faxcomex/IFaxOutgoingQueue::Blocked, faxcomex/IFaxOutgoingQueue::get_Blocked, faxcomex/IFaxOutgoingQueue::put_Blocked, put_Blocked
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
 - IFaxOutgoingQueue::put_Blocked
 - faxcomex/IFaxOutgoingQueue::put_Blocked
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
 - IFaxOutgoingQueue.Blocked
 - IFaxOutgoingQueue.get_Blocked
 - IFaxOutgoingQueue.put_Blocked
---

# IFaxOutgoingQueue::put_Blocked


## -description

The <b>IFaxOutgoingQueue::get_Blocked</b> property is a Boolean value that indicates whether the job queue for outgoing faxes is blocked. 

This property is read/write.

## -parameters

## -remarks

If this property is equal to <b>TRUE</b>, the outbound job queue is blocked and the fax service is not accepting outbound fax submissions. If this property is equal to <b>FALSE</b>, the queue is not blocked.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingqueue">IFaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-the-outgoing-queue-properties">Setting the Outgoing Queue Properties</a>
