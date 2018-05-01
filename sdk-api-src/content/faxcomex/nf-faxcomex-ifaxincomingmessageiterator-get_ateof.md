---
UID: NF:faxcomex.IFaxIncomingMessageIterator.get_AtEOF
title: IFaxIncomingMessageIterator::get_AtEOF method
author: windows-driver-content
description: The AtEOF property is the end of file marker for the archive of inbound fax messages.
old-location: fax\_mfax_faxincomingmessageiterator_ateof_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7orq.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: AtEOF property [Fax Service], AtEOF property [Fax Service], FaxIncomingMessageIterator object, FaxIncomingMessageIterator object [Fax Service], AtEOF property, IFaxIncomingMessageIterator, IFaxIncomingMessageIterator::get_AtEOF, _mfax_faxincomingmessageiterator.ateof, fax._mfax_faxincomingmessageiterator_ateof, fax._mfax_faxincomingmessageiterator_ateof_vb, get_AtEOF,IFaxIncomingMessageIterator.get_AtEOF
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	FaxIncomingMessageIterator.AtEOF
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingMessageIterator::get_AtEOF method


## -description


The <b>AtEOF</b> property is the end of file marker for the archive of inbound fax messages. If this property is equal to <b>True</b>, the archive cursor has moved beyond the last fax message in the inbound fax archive. If this property is equal to <b>False</b>, the archive cursor has not yet reached the end of the archive.

This property is read-only.


## -parameters


## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_IN_ARCHIVE</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/0969319b-7846-44a0-9667-161b326acea6">FaxIncomingMessageIterator</a>



<a href="https://msdn.microsoft.com/f0b3071b-6936-4b19-873b-0ab28cfaea93">IFaxIncomingMessageIterator</a>



<a href="https://msdn.microsoft.com/bdc7cdaa-0e37-4124-a9b3-9f9eabbe329e">Visual Basic Example</a>
 

 

