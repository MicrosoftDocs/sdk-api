---
UID: NF:faxcomex.IFaxIncomingMessageIterator.get_PrefetchSize
title: IFaxIncomingMessageIterator::get_PrefetchSize
author: windows-sdk-content
description: The PrefetchSize property indicates the size of the prefetch (read-ahead) buffer.
old-location: fax\_mfax_faxincomingmessageiterator_prefetchsize.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_64th.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxIncomingMessageIterator object [Fax Service],PrefetchSize property, FaxIncomingMessageIterator.PrefetchSize, IFaxIncomingMessageIterator.get_PrefetchSize, IFaxIncomingMessageIterator.put_PrefetchSize, IFaxIncomingMessageIterator::get_PrefetchSize, PrefetchSize property [Fax Service], PrefetchSize property [Fax Service],FaxIncomingMessageIterator object, _mfax_faxincomingmessageiterator.prefetchsize, fax._mfax_faxincomingmessageiterator_prefetchsize, get_PrefetchSize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxIncomingMessageIterator.PrefetchSize
 - IFaxIncomingMessageIterator.get_PrefetchSize
 - IFaxIncomingMessageIterator.put_PrefetchSize
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingMessageIterator::get_PrefetchSize


## -description


The <b>PrefetchSize</b> property indicates the size of the prefetch (read-ahead) buffer.

This property is read/write.


## -parameters


## -remarks



The prefetch buffer contains messages and makes the iteration process more efficient because you iterate through the buffer rather than through a folder. 

Changes you make to the size of the prefetch buffer take place immediately because <a href="https://msdn.microsoft.com/0969319b-7846-44a0-9667-161b326acea6">FaxIncomingMessageIterator</a> is a local object.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_IN_ARCHIVE</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/0969319b-7846-44a0-9667-161b326acea6">FaxIncomingMessageIterator</a>



<a href="https://msdn.microsoft.com/0b9280dc-5895-4c11-9298-459b7792ad39">PrefetchSize</a>



<a href="https://msdn.microsoft.com/bdc7cdaa-0e37-4124-a9b3-9f9eabbe329e">Visual Basic Example</a>
 

 

