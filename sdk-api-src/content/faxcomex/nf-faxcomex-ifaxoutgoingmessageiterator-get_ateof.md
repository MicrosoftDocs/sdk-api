---
UID: NF:faxcomex.IFaxOutgoingMessageIterator.get_AtEOF
title: IFaxOutgoingMessageIterator::get_AtEOF
author: windows-driver-content
description: The AtEOF property is the end-of-file marker for the archive of outbound fax messages.
old-location: fax\_mfax_faxoutgoingmessageiterator_ateof_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_3w6e.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: AtEOF property [Fax Service], AtEOF property [Fax Service],FaxOutgoingMessageIterator object, FaxOutgoingMessageIterator object [Fax Service],AtEOF property, FaxOutgoingMessageIterator.AtEOF, IFaxOutgoingMessageIterator.get_AtEOF, IFaxOutgoingMessageIterator::get_AtEOF, _mfax_faxoutgoingmessageiterator.ateof, fax._mfax_faxoutgoingmessageiterator_ateof, fax._mfax_faxoutgoingmessageiterator_ateof_vb, get_AtEOF
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
-	FaxOutgoingMessageIterator.AtEOF
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingMessageIterator::get_AtEOF


## -description


The AtEOF property is the end-of-file marker for the archive of outbound fax messages.

This property is read-only.


## -parameters


## -remarks



If this property is equal to <b>True</b>, the archive cursor has moved beyond the last fax message in the archive. If this property is equal to <b>False</b>, the archive cursor has not reached the end of the archive.




## -see-also




<a href="https://msdn.microsoft.com/4eab8319-23ff-4f25-9402-bcb53a440879">FaxOutgoingMessageIterator</a>



<a href="https://msdn.microsoft.com/5a34e012-33ae-4950-9f10-a3ad94142ef1">IFaxOutgoingMessageIterator</a>



<a href="https://msdn.microsoft.com/072eb2cc-7fd9-4f8e-8583-44384357e708">Visual Basic Example</a>
 

 

