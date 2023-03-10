---
UID: NF:faxcomex.IFaxIncomingMessageIterator.MoveNext
title: IFaxIncomingMessageIterator::MoveNext (faxcomex.h)
description: The MoveNext method moves the archive cursor to the next message in the archive of inbound faxes.
helpviewer_keywords: ["IFaxIncomingMessageIterator interface [Fax Service]","MoveNext method","IFaxIncomingMessageIterator.MoveNext","IFaxIncomingMessageIterator::MoveNext","MoveNext","MoveNext method [Fax Service]","MoveNext method [Fax Service]","IFaxIncomingMessageIterator interface","_mfax_faxincomingmessageiterator.movenext","fax._mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_movenext_cpp","fax._mfax_faxincomingmessageiterator_movenext","faxcomex/IFaxIncomingMessageIterator::MoveNext"]
old-location: fax\_mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_movenext_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_27lg.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessageIterator interface [Fax Service],MoveNext method, IFaxIncomingMessageIterator.MoveNext, IFaxIncomingMessageIterator::MoveNext, MoveNext, MoveNext method [Fax Service], MoveNext method [Fax Service],IFaxIncomingMessageIterator interface, _mfax_faxincomingmessageiterator.movenext, fax._mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_movenext_cpp, fax._mfax_faxincomingmessageiterator_movenext, faxcomex/IFaxIncomingMessageIterator::MoveNext
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
 - IFaxIncomingMessageIterator::MoveNext
 - faxcomex/IFaxIncomingMessageIterator::MoveNext
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
 - IFaxIncomingMessageIterator.MoveNext
 - IFaxIncomingMessageIterator.MoveNext
---

# IFaxIncomingMessageIterator::MoveNext


## -description

The <b>MoveNext</b> method moves the archive cursor to the next message in the archive of inbound faxes.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can make the iteration process more efficient by using a prefetch buffer. A prefetch buffer contains messages and allows you to iterate through the buffer rather than through a folder. Set the size of the buffer (the number of messages to be held in the buffer) using the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator-prefetchsize">PrefetchSize</a> property.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_IN_ARCHIVE</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator">FaxIncomingMessageIterator</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>
