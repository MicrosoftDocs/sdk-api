---
UID: NF:faxcomex.IFaxOutgoingQueue.put_Paused
title: IFaxOutgoingQueue::put_Paused (faxcomex.h)
description: The IFaxOutgoingQueue::get_Paused property is a Boolean value that indicates whether the job queue for outgoing faxes is paused. (Put)
helpviewer_keywords: ["IFaxOutgoingQueue interface [Fax Service]","Paused property","IFaxOutgoingQueue.Paused","IFaxOutgoingQueue.get_Paused","IFaxOutgoingQueue.put_Paused","IFaxOutgoingQueue::Paused","IFaxOutgoingQueue::get_Paused","IFaxOutgoingQueue::put_Paused","Paused property [Fax Service]","Paused property [Fax Service]","IFaxOutgoingQueue interface","_mfax_faxoutgoingqueue.paused","fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_paused_cpp","fax._mfax_faxoutgoingqueue_paused","faxcomex/IFaxOutgoingQueue::Paused","faxcomex/IFaxOutgoingQueue::get_Paused","faxcomex/IFaxOutgoingQueue::put_Paused","put_Paused"]
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_paused_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_81b8.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingQueue interface [Fax Service],Paused property, IFaxOutgoingQueue.Paused, IFaxOutgoingQueue.get_Paused, IFaxOutgoingQueue.put_Paused, IFaxOutgoingQueue::Paused, IFaxOutgoingQueue::get_Paused, IFaxOutgoingQueue::put_Paused, Paused property [Fax Service], Paused property [Fax Service],IFaxOutgoingQueue interface, _mfax_faxoutgoingqueue.paused, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_paused_cpp, fax._mfax_faxoutgoingqueue_paused, faxcomex/IFaxOutgoingQueue::Paused, faxcomex/IFaxOutgoingQueue::get_Paused, faxcomex/IFaxOutgoingQueue::put_Paused, put_Paused
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
 - IFaxOutgoingQueue::put_Paused
 - faxcomex/IFaxOutgoingQueue::put_Paused
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
 - IFaxOutgoingQueue.Paused
 - IFaxOutgoingQueue.get_Paused
 - IFaxOutgoingQueue.put_Paused
 - IFaxOutgoingQueue.get_Paused
 - IFaxOutgoingQueue.put_Paused
---

# IFaxOutgoingQueue::put_Paused


## -description

The <b>IFaxOutgoingQueue::get_Paused</b> property is a Boolean value that indicates whether the job queue for outgoing faxes is paused. 

This property is read/write.

## -parameters

## -remarks

If this property is equal to <b>TRUE</b>, the job queue is paused and the fax service is not processing jobs in the queue. If this property is equal to <b>FALSE</b>, the outgoing queue is not paused.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingqueue">IFaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-the-outgoing-queue-properties">Setting the Outgoing Queue Properties</a>
