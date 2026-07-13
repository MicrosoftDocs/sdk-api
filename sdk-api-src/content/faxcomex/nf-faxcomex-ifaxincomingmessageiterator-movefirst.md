---
UID: NF:faxcomex.IFaxIncomingMessageIterator.MoveFirst
title: IFaxIncomingMessageIterator::MoveFirst (faxcomex.h)
description: The MoveFirst method moves the archive cursor to the first fax message in the archive of inbound faxes.
helpviewer_keywords: ["IFaxIncomingMessageIterator interface [Fax Service]","MoveFirst method","IFaxIncomingMessageIterator.MoveFirst","IFaxIncomingMessageIterator::MoveFirst","MoveFirst","MoveFirst method [Fax Service]","MoveFirst method [Fax Service]","IFaxIncomingMessageIterator interface","_mfax_faxincomingmessageiterator.movefirst","fax._mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_movefirst_cpp","fax._mfax_faxincomingmessageiterator_movefirst","faxcomex/IFaxIncomingMessageIterator::MoveFirst"]
old-location: fax\_mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_movefirst_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6p84.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessageIterator interface [Fax Service],MoveFirst method, IFaxIncomingMessageIterator.MoveFirst, IFaxIncomingMessageIterator::MoveFirst, MoveFirst, MoveFirst method [Fax Service], MoveFirst method [Fax Service],IFaxIncomingMessageIterator interface, _mfax_faxincomingmessageiterator.movefirst, fax._mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_movefirst_cpp, fax._mfax_faxincomingmessageiterator_movefirst, faxcomex/IFaxIncomingMessageIterator::MoveFirst
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
 - IFaxIncomingMessageIterator::MoveFirst
 - faxcomex/IFaxIncomingMessageIterator::MoveFirst
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
 - IFaxIncomingMessageIterator.MoveFirst
 - IFaxIncomingMessageIterator.MoveFirst
---

# IFaxIncomingMessageIterator::MoveFirst


## -description

The <b>MoveFirst</b> method moves the archive cursor to the first fax message in the archive of inbound faxes.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_IN_ARCHIVE</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator">FaxIncomingMessageIterator</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>
