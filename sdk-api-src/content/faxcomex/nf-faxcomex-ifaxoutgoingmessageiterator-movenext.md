---
UID: NF:faxcomex.IFaxOutgoingMessageIterator.MoveNext
title: IFaxOutgoingMessageIterator::MoveNext (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutgoingMessageIterator::MoveNext method moves the archive cursor to the next fax message in the outbound archive.
old-location: fax\_mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_movenext_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5b04.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingMessageIterator interface [Fax Service],MoveNext method, IFaxOutgoingMessageIterator.MoveNext, IFaxOutgoingMessageIterator::MoveNext, MoveNext, MoveNext method [Fax Service], MoveNext method [Fax Service],IFaxOutgoingMessageIterator interface, _mfax_faxoutgoingmessageiterator.movenext, fax._mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_movenext_cpp, fax._mfax_faxoutgoingmessageiterator_movenext, faxcomex/IFaxOutgoingMessageIterator::MoveNext
ms.topic: method
f1_keywords: 
 - "faxcomex/IFaxOutgoingMessageIterator.MoveNext"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingMessageIterator.MoveNext
 - IFaxOutgoingMessageIterator.MoveNext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutgoingMessageIterator::MoveNext


## -description


The <b>IFaxOutgoingMessageIterator::MoveNext</b> method moves the archive cursor to the next fax message in the outbound archive.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The method will fail if the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator-ateof-vb">IFaxOutgoingMessageIterator::get_AtEOF</a> property is equal to <b>TRUE</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator">FaxOutgoingMessageIterator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-outgoing-archive">Visual Basic Example</a>
 

 

