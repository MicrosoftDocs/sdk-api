---
UID: NF:faxcomex.IFaxOutgoingMessageIterator.get_Message
title: IFaxOutgoingMessageIterator::get_Message (faxcomex.h)
description: The IFaxOutgoingMessageIterator::get_Message property retrieves the outbound fax message under the archive cursor.
helpviewer_keywords: ["IFaxOutgoingMessageIterator interface [Fax Service]","Message property","IFaxOutgoingMessageIterator.Message","IFaxOutgoingMessageIterator.get_Message","IFaxOutgoingMessageIterator::Message","IFaxOutgoingMessageIterator::get_Message","Message property [Fax Service]","Message property [Fax Service]","IFaxOutgoingMessageIterator interface","_mfax_faxoutgoingmessageiterator.message_cpp","fax._mfax_faxoutgoingmessageiterator_message_cpp","faxcomex/IFaxOutgoingMessageIterator::Message","faxcomex/IFaxOutgoingMessageIterator::get_Message","get_Message"]
old-location: fax\_mfax_faxoutgoingmessageiterator_message_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7wkl_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingMessageIterator interface [Fax Service],Message property, IFaxOutgoingMessageIterator.Message, IFaxOutgoingMessageIterator.get_Message, IFaxOutgoingMessageIterator::Message, IFaxOutgoingMessageIterator::get_Message, Message property [Fax Service], Message property [Fax Service],IFaxOutgoingMessageIterator interface, _mfax_faxoutgoingmessageiterator.message_cpp, fax._mfax_faxoutgoingmessageiterator_message_cpp, faxcomex/IFaxOutgoingMessageIterator::Message, faxcomex/IFaxOutgoingMessageIterator::get_Message, get_Message
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
 - IFaxOutgoingMessageIterator::get_Message
 - faxcomex/IFaxOutgoingMessageIterator::get_Message
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
 - IFaxOutgoingMessageIterator.Message
 - IFaxOutgoingMessageIterator.get_Message
---

# IFaxOutgoingMessageIterator::get_Message


## -description

The <b>IFaxOutgoingMessageIterator::get_Message</b> property retrieves the outbound fax message under the archive cursor.

This property is read-only.

## -parameters

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> and <b>farQUERY_OUT_ARCHIVE</b> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator">FaxOutgoingMessageIterator</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-outgoing-archive">Visual Basic Example</a>