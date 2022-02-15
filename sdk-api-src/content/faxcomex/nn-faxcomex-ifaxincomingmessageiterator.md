---
UID: NN:faxcomex.IFaxIncomingMessageIterator
title: IFaxIncomingMessageIterator (faxcomex.h)
description: The IFaxIncomingMessageIterator interface is used by a fax client application to move through the archive of inbound fax messages that the fax service has successfully received.
helpviewer_keywords: ["IFaxIncomingMessageIterator","IFaxIncomingMessageIterator interface [Fax Service]","IFaxIncomingMessageIterator interface [Fax Service]","described","_mfax_faxincomingmessageiterator_cpp","fax._mfax_faxincomingmessageiterator_cpp","faxcomex/IFaxIncomingMessageIterator"]
old-location: fax\_mfax_faxincomingmessageiterator_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9zg2_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessageIterator, IFaxIncomingMessageIterator interface [Fax Service], IFaxIncomingMessageIterator interface [Fax Service],described, _mfax_faxincomingmessageiterator_cpp, fax._mfax_faxincomingmessageiterator_cpp, faxcomex/IFaxIncomingMessageIterator
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
 - IFaxIncomingMessageIterator
 - faxcomex/IFaxIncomingMessageIterator
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
 - IFaxIncomingMessageIterator
---

# IFaxIncomingMessageIterator interface


## -description

The <b>IFaxIncomingMessageIterator</b> interface is used by a fax client application to move through the archive of inbound fax messages that the fax service has successfully received. Because the <b>IFaxIncomingMessageIterator</b> interface is a forward iterator, you can only move forward through the archive from beginning to end, and you can access only one fax message (<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage">IFaxIncomingMessage</a> object) at a time.

The <b>IFaxIncomingMessageIterator</b> interface is accessed through the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a> interface.

## -inheritance

The <b>IFaxIncomingMessageIterator</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxIncomingMessageIterator</b> also has these types of members:

## -remarks

To create a <b>FaxIncomingMessageIterator</b> object in C++, call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-getmessages-vb">IFaxIncomingArchive::GetMessages</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator">FaxIncomingMessageIterator</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>
