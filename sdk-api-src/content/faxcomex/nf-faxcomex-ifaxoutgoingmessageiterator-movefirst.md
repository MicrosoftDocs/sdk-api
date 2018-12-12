---
UID: NF:faxcomex.IFaxOutgoingMessageIterator.MoveFirst
title: IFaxOutgoingMessageIterator::MoveFirst
author: windows-sdk-content
description: The IFaxOutgoingMessageIterator::MoveFirst method moves the archive cursor to the first fax message in the outbound archive.
old-location: fax\_mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_movefirst_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4ras.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxOutgoingMessageIterator interface [Fax Service],MoveFirst method, IFaxOutgoingMessageIterator.MoveFirst, IFaxOutgoingMessageIterator::MoveFirst, MoveFirst, MoveFirst method [Fax Service], MoveFirst method [Fax Service],IFaxOutgoingMessageIterator interface, _mfax_faxoutgoingmessageiterator.movefirst, fax._mfax_faxoutgoingmessageiterator_cpp_mfax_faxoutgoingmessageiterator_movefirst_cpp, fax._mfax_faxoutgoingmessageiterator_movefirst, faxcomex/IFaxOutgoingMessageIterator::MoveFirst
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
 - IFaxOutgoingMessageIterator.MoveFirst
 - IFaxOutgoingMessageIterator.MoveFirst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingMessageIterator::MoveFirst


## -description


The <b>IFaxOutgoingMessageIterator::MoveFirst</b> method moves the archive cursor to the first fax message in the outbound archive.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> and <b>farQUERY_OUT_ARCHIVE</b> access rights.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690094(v=VS.85).aspx">FaxOutgoingMessageIterator</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690096(v=VS.85).aspx">IFaxOutgoingMessageIterator</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693402(v=VS.85).aspx">Visual Basic Example</a>
 

 

