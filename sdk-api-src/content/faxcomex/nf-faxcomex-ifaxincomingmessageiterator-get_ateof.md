---
UID: NF:faxcomex.IFaxIncomingMessageIterator.get_AtEOF
title: IFaxIncomingMessageIterator::get_AtEOF (faxcomex.h)
description: The AtEOF property is the end of file marker for the archive of inbound fax messages.
helpviewer_keywords: ["AtEOF property [Fax Service]","AtEOF property [Fax Service]","IFaxIncomingMessageIterator interface","IFaxIncomingMessageIterator interface [Fax Service]","AtEOF property","IFaxIncomingMessageIterator.AtEOF","IFaxIncomingMessageIterator.get_AtEOF","IFaxIncomingMessageIterator::AtEOF","IFaxIncomingMessageIterator::get_AtEOF","_mfax_faxincomingmessageiterator.ateof","fax._mfax_faxincomingmessageiterator_ateof","fax._mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_ateof_cpp","faxcomex/IFaxIncomingMessageIterator::AtEOF","faxcomex/IFaxIncomingMessageIterator::get_AtEOF","get_AtEOF"]
old-location: fax\_mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_ateof_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7orq.htm
ms.date: 12/05/2018
ms.keywords: AtEOF property [Fax Service], AtEOF property [Fax Service],IFaxIncomingMessageIterator interface, IFaxIncomingMessageIterator interface [Fax Service],AtEOF property, IFaxIncomingMessageIterator.AtEOF, IFaxIncomingMessageIterator.get_AtEOF, IFaxIncomingMessageIterator::AtEOF, IFaxIncomingMessageIterator::get_AtEOF, _mfax_faxincomingmessageiterator.ateof, fax._mfax_faxincomingmessageiterator_ateof, fax._mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_ateof_cpp, faxcomex/IFaxIncomingMessageIterator::AtEOF, faxcomex/IFaxIncomingMessageIterator::get_AtEOF, get_AtEOF
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
 - IFaxIncomingMessageIterator::get_AtEOF
 - faxcomex/IFaxIncomingMessageIterator::get_AtEOF
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
 - IFaxIncomingMessageIterator.AtEOF
 - IFaxIncomingMessageIterator.get_AtEOF
---

# IFaxIncomingMessageIterator::get_AtEOF


## -description

The <b>AtEOF</b> property is the end of file marker for the archive of inbound fax messages. If this property is equal to <b>TRUE</b>, the archive cursor has moved beyond the last fax message in the inbound fax archive. If this property is equal to <b>FALSE</b>, the archive cursor has not yet reached the end of the archive.

This property is read-only.

## -parameters

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_IN_ARCHIVE</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator">FaxIncomingMessageIterator</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>