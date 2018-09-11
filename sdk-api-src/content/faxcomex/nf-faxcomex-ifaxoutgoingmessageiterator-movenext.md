---
UID: NF:faxcomex.IFaxOutgoingMessageIterator.MoveNext
title: IFaxOutgoingMessageIterator::MoveNext
author: windows-sdk-content
description: The IFaxOutgoingMessageIterator::MoveNext method moves the archive cursor to the next fax message in the outbound archive.
old-location: fax\_mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_movenext_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5b04.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxOutgoingMessageIterator interface [Fax Service],MoveNext method, IFaxOutgoingMessageIterator.MoveNext, IFaxOutgoingMessageIterator::MoveNext, MoveNext, MoveNext method [Fax Service], MoveNext method [Fax Service],IFaxOutgoingMessageIterator interface, _mfax_faxoutgoingmessageiterator.movenext, fax._mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_movenext_cpp, fax._mfax_faxoutgoingmessageiterator_movenext, faxcomex/IFaxOutgoingMessageIterator::MoveNext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IFaxOutgoingMessageIterator::MoveNext


## -description


The <b>IFaxOutgoingMessageIterator::MoveNext</b> method moves the archive cursor to the next fax message in the outbound archive.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The method will fail if the <a href="https://msdn.microsoft.com/f4b4bfbd-041a-4495-8d4e-fcb81b83bb7e">IFaxOutgoingMessageIterator::get_AtEOF</a> property is equal to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/4eab8319-23ff-4f25-9402-bcb53a440879">FaxOutgoingMessageIterator</a>



<a href="https://msdn.microsoft.com/5a34e012-33ae-4950-9f10-a3ad94142ef1">IFaxOutgoingMessageIterator</a>



<a href="https://msdn.microsoft.com/072eb2cc-7fd9-4f8e-8583-44384357e708">Visual Basic Example</a>
 

 

