---
UID: NF:faxcomex.IFaxOutgoingMessageIterator.get_AtEOF
title: IFaxOutgoingMessageIterator::get_AtEOF (faxcomex.h)
description: The AtEOF property is the end-of-file marker for the archive of outbound fax messages.
helpviewer_keywords: ["AtEOF property [Fax Service]","AtEOF property [Fax Service]","IFaxOutgoingMessageIterator interface","IFaxOutgoingMessageIterator interface [Fax Service]","AtEOF property","IFaxOutgoingMessageIterator.AtEOF","IFaxOutgoingMessageIterator.get_AtEOF","IFaxOutgoingMessageIterator::AtEOF","IFaxOutgoingMessageIterator::get_AtEOF","_mfax_faxoutgoingmessageiterator.ateof","fax._mfax_faxoutgoingmessageiterator_ateof","fax._mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_ateof_cpp","faxcomex/IFaxOutgoingMessageIterator::AtEOF","faxcomex/IFaxOutgoingMessageIterator::get_AtEOF","get_AtEOF"]
old-location: fax\_mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_ateof_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_3w6e.htm
ms.date: 12/05/2018
ms.keywords: AtEOF property [Fax Service], AtEOF property [Fax Service],IFaxOutgoingMessageIterator interface, IFaxOutgoingMessageIterator interface [Fax Service],AtEOF property, IFaxOutgoingMessageIterator.AtEOF, IFaxOutgoingMessageIterator.get_AtEOF, IFaxOutgoingMessageIterator::AtEOF, IFaxOutgoingMessageIterator::get_AtEOF, _mfax_faxoutgoingmessageiterator.ateof, fax._mfax_faxoutgoingmessageiterator_ateof, fax._mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_ateof_cpp, faxcomex/IFaxOutgoingMessageIterator::AtEOF, faxcomex/IFaxOutgoingMessageIterator::get_AtEOF, get_AtEOF
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
 - IFaxOutgoingMessageIterator::get_AtEOF
 - faxcomex/IFaxOutgoingMessageIterator::get_AtEOF
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
 - IFaxOutgoingMessageIterator.AtEOF
 - IFaxOutgoingMessageIterator.get_AtEOF
---

# IFaxOutgoingMessageIterator::get_AtEOF


## -description

The AtEOF property is the end-of-file marker for the archive of outbound fax messages.

This property is read-only.

## -parameters

## -remarks

If this property is equal to <b>TRUE</b>, the archive cursor has moved beyond the last fax message in the archive. If this property is equal to <b>FALSE</b>, the archive cursor has not reached the end of the archive.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator">FaxOutgoingMessageIterator</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-outgoing-archive">Visual Basic Example</a>