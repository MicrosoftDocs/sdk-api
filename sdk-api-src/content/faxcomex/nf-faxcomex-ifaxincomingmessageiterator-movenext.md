---
UID: NF:faxcomex.IFaxIncomingMessageIterator.MoveNext
title: IFaxIncomingMessageIterator::MoveNext
author: windows-sdk-content
description: The MoveNext method moves the archive cursor to the next message in the archive of inbound faxes.
old-location: fax\_mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_movenext_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_27lg.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IFaxIncomingMessageIterator interface [Fax Service],MoveNext method, IFaxIncomingMessageIterator.MoveNext, IFaxIncomingMessageIterator::MoveNext, MoveNext, MoveNext method [Fax Service], MoveNext method [Fax Service],IFaxIncomingMessageIterator interface, _mfax_faxincomingmessageiterator.movenext, fax._mfax_faxincomingmessageiterator_cpp_mfax_faxincomingmessageiterator_movenext_cpp, fax._mfax_faxincomingmessageiterator_movenext, faxcomex/IFaxIncomingMessageIterator::MoveNext
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
 - IFaxIncomingMessageIterator.MoveNext
 - IFaxIncomingMessageIterator.MoveNext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingMessageIterator::MoveNext


## -description


The <b>MoveNext</b> method moves the archive cursor to the next message in the archive of inbound faxes.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can make the iteration process more efficient by using a prefetch buffer. A prefetch buffer contains messages and allows you to iterate through the buffer rather than through a folder. Set the size of the buffer (the number of messages to be held in the buffer) using the <a href="https://msdn.microsoft.com/0dc10f14-1ae3-47e5-aab2-53ddaa45b8a0">PrefetchSize</a> property.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_IN_ARCHIVE</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/0969319b-7846-44a0-9667-161b326acea6">FaxIncomingMessageIterator</a>



<a href="https://msdn.microsoft.com/f0b3071b-6936-4b19-873b-0ab28cfaea93">IFaxIncomingMessageIterator</a>



<a href="https://msdn.microsoft.com/bdc7cdaa-0e37-4124-a9b3-9f9eabbe329e">Visual Basic Example</a>
 

 

