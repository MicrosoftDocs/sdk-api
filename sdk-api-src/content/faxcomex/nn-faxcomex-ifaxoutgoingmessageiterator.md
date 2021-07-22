---
UID: NN:faxcomex.IFaxOutgoingMessageIterator
title: IFaxOutgoingMessageIterator (faxcomex.h)
description: The IFaxOutgoingMessageIterator interface describes an object that is used by a fax client application to move through the archive of fax messages that the fax service has successfully transmitted, represented by FaxOutgoingMessage objects.
helpviewer_keywords: ["IFaxOutgoingMessageIterator","IFaxOutgoingMessageIterator interface [Fax Service]","IFaxOutgoingMessageIterator interface [Fax Service]","described","_mfax_faxoutgoingmessageiterator_cpp","fax._mfax_faxoutgoingmessageiterator_cpp","faxcomex/IFaxOutgoingMessageIterator"]
old-location: fax\_mfax_faxoutgoingmessageiterator_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8euq_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingMessageIterator, IFaxOutgoingMessageIterator interface [Fax Service], IFaxOutgoingMessageIterator interface [Fax Service],described, _mfax_faxoutgoingmessageiterator_cpp, fax._mfax_faxoutgoingmessageiterator_cpp, faxcomex/IFaxOutgoingMessageIterator
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
 - IFaxOutgoingMessageIterator
 - faxcomex/IFaxOutgoingMessageIterator
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
 - IFaxOutgoingMessageIterator
---

# IFaxOutgoingMessageIterator interface


## -description

The <b>IFaxOutgoingMessageIterator</b> interface describes an object that is used by a fax client application to move through the archive of fax messages that the fax service has successfully transmitted, represented by <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a> objects. Because the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator">FaxOutgoingMessageIterator</a> object is a forward iterator, you can only move forward through the archive, from beginning to end, and you can access only one message at a time.

## -inheritance

The <b>IFaxOutgoingMessageIterator</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutgoingMessageIterator</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxOutgoingMessageIterator</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator">FaxOutgoingMessageIterator</a> object.
