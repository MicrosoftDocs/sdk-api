---
UID: NN:faxcomex.IFaxIncomingMessage
title: IFaxIncomingMessage (faxcomex.h)
description: Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes. (IFaxIncomingMessage)
helpviewer_keywords: ["IFaxIncomingMessage","IFaxIncomingMessage interface [Fax Service]","IFaxIncomingMessage interface [Fax Service]","described","_mfax_faxincomingmessage_cpp","fax._mfax_faxincomingmessage_cpp","faxcomex/IFaxIncomingMessage"]
old-location: fax\_mfax_faxincomingmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_44h1_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessage, IFaxIncomingMessage interface [Fax Service], IFaxIncomingMessage interface [Fax Service],described, _mfax_faxincomingmessage_cpp, fax._mfax_faxincomingmessage_cpp, faxcomex/IFaxIncomingMessage
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
 - IFaxIncomingMessage
 - faxcomex/IFaxIncomingMessage
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
 - IFaxIncomingMessage
---

# IFaxIncomingMessage interface


## -description

Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes. The archive contains faxes received successfully by the fax service. The interface also includes methods to delete a message from the archive and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with the fax message to a file on the local computer.

The <b>IFaxIncomingMessage</b> interface is accessed through the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a> interface or <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a> interface.

## -inheritance

The <b>IFaxIncomingMessage</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxIncomingMessage</b> also has these types of members:

## -remarks

To create a <b>FaxIncomingMessage</b> object in C++, call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-getmessage-vb">IFaxIncomingArchive::GetMessage</a> method or the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator-message-vb">IFaxIncomingMessageIterator::get_Message</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a>
