---
UID: NF:faxcomex.IFaxOutgoingQueue.put_AgeLimit
title: IFaxOutgoingQueue::put_AgeLimit (faxcomex.h)
description: The IFaxOutgoingQueue::get_AgeLimit property is a value that indicates the number of days that the fax service retains an unsent job in the fax job queue. (Put)
helpviewer_keywords: ["AgeLimit property [Fax Service]","AgeLimit property [Fax Service]","IFaxOutgoingQueue interface","IFaxOutgoingQueue interface [Fax Service]","AgeLimit property","IFaxOutgoingQueue.AgeLimit","IFaxOutgoingQueue.put_AgeLimit","IFaxOutgoingQueue::AgeLimit","IFaxOutgoingQueue::get_AgeLimit","IFaxOutgoingQueue::put_AgeLimit","_mfax_faxoutgoingqueue.agelimit","fax._mfax_faxoutgoingqueue_agelimit","fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_agelimit_cpp","faxcomex/IFaxOutgoingQueue::AgeLimit","faxcomex/IFaxOutgoingQueue::get_AgeLimit","faxcomex/IFaxOutgoingQueue::put_AgeLimit","put_AgeLimit"]
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_agelimit_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7qyc.htm
ms.date: 12/05/2018
ms.keywords: AgeLimit property [Fax Service], AgeLimit property [Fax Service],IFaxOutgoingQueue interface, IFaxOutgoingQueue interface [Fax Service],AgeLimit property, IFaxOutgoingQueue.AgeLimit, IFaxOutgoingQueue.put_AgeLimit, IFaxOutgoingQueue::AgeLimit, IFaxOutgoingQueue::get_AgeLimit, IFaxOutgoingQueue::put_AgeLimit, _mfax_faxoutgoingqueue.agelimit, fax._mfax_faxoutgoingqueue_agelimit, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_agelimit_cpp, faxcomex/IFaxOutgoingQueue::AgeLimit, faxcomex/IFaxOutgoingQueue::get_AgeLimit, faxcomex/IFaxOutgoingQueue::put_AgeLimit, put_AgeLimit
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
 - IFaxOutgoingQueue::put_AgeLimit
 - faxcomex/IFaxOutgoingQueue::put_AgeLimit
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
 - IFaxOutgoingQueue.AgeLimit
 - IFaxOutgoingQueue.get_AgeLimit
 - IFaxOutgoingQueue.put_AgeLimit
---

# IFaxOutgoingQueue::put_AgeLimit


## -description

The <b>IFaxOutgoingQueue::get_AgeLimit</b> property is a value that indicates the number of days that the fax service retains an unsent job in the fax job queue. 

This property is read/write.

## -parameters

## -remarks

If the fax job remains in the outbound job queue longer than the value specified, the fax service deletes the job. If the value of this property is zero, the fax service does not enforce an age limit.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingqueue">IFaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-the-outgoing-queue-properties">Setting the Outgoing Queue Properties</a>
