---
UID: NF:faxcomex.IFaxOutgoingQueue.get_AllowPersonalCoverPages
title: IFaxOutgoingQueue::get_AllowPersonalCoverPages (faxcomex.h)
description: The AllowPersonalCoverPages property is a Boolean value that indicates whether fax client applications can include a user-designed cover page with fax transmissions. (Get)
helpviewer_keywords: ["AllowPersonalCoverPages property [Fax Service]","AllowPersonalCoverPages property [Fax Service]","IFaxOutgoingQueue interface","IFaxOutgoingQueue interface [Fax Service]","AllowPersonalCoverPages property","IFaxOutgoingQueue.AllowPersonalCoverPages","IFaxOutgoingQueue.get_AllowPersonalCoverPages","IFaxOutgoingQueue::AllowPersonalCoverPages","IFaxOutgoingQueue::get_AllowPersonalCoverPages","IFaxOutgoingQueue::put_AllowPersonalCoverPages","_mfax_faxoutgoingqueue.allowpersonalcoverpages","fax._mfax_faxoutgoingqueue_allowpersonalcoverpages","fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_allowpersonalcoverpages_cpp","faxcomex/IFaxOutgoingQueue::AllowPersonalCoverPages","faxcomex/IFaxOutgoingQueue::get_AllowPersonalCoverPages","faxcomex/IFaxOutgoingQueue::put_AllowPersonalCoverPages","get_AllowPersonalCoverPages"]
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_allowpersonalcoverpages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5cc3.htm
ms.date: 12/05/2018
ms.keywords: AllowPersonalCoverPages property [Fax Service], AllowPersonalCoverPages property [Fax Service],IFaxOutgoingQueue interface, IFaxOutgoingQueue interface [Fax Service],AllowPersonalCoverPages property, IFaxOutgoingQueue.AllowPersonalCoverPages, IFaxOutgoingQueue.get_AllowPersonalCoverPages, IFaxOutgoingQueue::AllowPersonalCoverPages, IFaxOutgoingQueue::get_AllowPersonalCoverPages, IFaxOutgoingQueue::put_AllowPersonalCoverPages, _mfax_faxoutgoingqueue.allowpersonalcoverpages, fax._mfax_faxoutgoingqueue_allowpersonalcoverpages, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_allowpersonalcoverpages_cpp, faxcomex/IFaxOutgoingQueue::AllowPersonalCoverPages, faxcomex/IFaxOutgoingQueue::get_AllowPersonalCoverPages, faxcomex/IFaxOutgoingQueue::put_AllowPersonalCoverPages, get_AllowPersonalCoverPages
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
 - IFaxOutgoingQueue::get_AllowPersonalCoverPages
 - faxcomex/IFaxOutgoingQueue::get_AllowPersonalCoverPages
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
 - IFaxOutgoingQueue.AllowPersonalCoverPages
 - IFaxOutgoingQueue.get_AllowPersonalCoverPages
 - IFaxOutgoingQueue.put_AllowPersonalCoverPages
---

# IFaxOutgoingQueue::get_AllowPersonalCoverPages


## -description

The AllowPersonalCoverPages property is a Boolean value that indicates whether fax client applications can include a user-designed cover page with fax transmissions.

This property is read/write.

## -parameters

## -remarks

If this property is equal to <b>TRUE</b>, clients can include personal cover page files with fax transmissions. If this property is equal to <b>FALSE</b>, clients must use a common cover page file stored on the fax server. 

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingqueue">IFaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-the-outgoing-queue-properties">Setting the Outgoing Queue Properties</a>
