---
UID: NF:faxcomex.IFaxOutgoingMessageIterator.MoveFirst
title: IFaxOutgoingMessageIterator::MoveFirst (faxcomex.h)
description: The IFaxOutgoingMessageIterator::MoveFirst method moves the archive cursor to the first fax message in the outbound archive.
helpviewer_keywords: ["IFaxOutgoingMessageIterator interface [Fax Service]","MoveFirst method","IFaxOutgoingMessageIterator.MoveFirst","IFaxOutgoingMessageIterator::MoveFirst","MoveFirst","MoveFirst method [Fax Service]","MoveFirst method [Fax Service]","IFaxOutgoingMessageIterator interface","_mfax_faxoutgoingmessageiterator.movefirst","fax._mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_movefirst_cpp","fax._mfax_faxoutgoingmessageiterator_movefirst","faxcomex/IFaxOutgoingMessageIterator::MoveFirst"]
old-location: fax\_mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_movefirst_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4ras.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingMessageIterator interface [Fax Service],MoveFirst method, IFaxOutgoingMessageIterator.MoveFirst, IFaxOutgoingMessageIterator::MoveFirst, MoveFirst, MoveFirst method [Fax Service], MoveFirst method [Fax Service],IFaxOutgoingMessageIterator interface, _mfax_faxoutgoingmessageiterator.movefirst, fax._mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_movefirst_cpp, fax._mfax_faxoutgoingmessageiterator_movefirst, faxcomex/IFaxOutgoingMessageIterator::MoveFirst
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
 - IFaxOutgoingMessageIterator::MoveFirst
 - faxcomex/IFaxOutgoingMessageIterator::MoveFirst
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
 - IFaxOutgoingMessageIterator.MoveFirst
 - IFaxOutgoingMessageIterator.MoveFirst
---

# IFaxOutgoingMessageIterator::MoveFirst


## -description

The <b>IFaxOutgoingMessageIterator::MoveFirst</b> method moves the archive cursor to the first fax message in the outbound archive.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> and <b>farQUERY_OUT_ARCHIVE</b> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator">FaxOutgoingMessageIterator</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-outgoing-archive">Visual Basic Example</a>
