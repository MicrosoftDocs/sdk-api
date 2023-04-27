---
UID: NF:faxcomex.IFaxIncomingMessageIterator.get_PrefetchSize
title: IFaxIncomingMessageIterator::get_PrefetchSize (faxcomex.h)
description: The PrefetchSize property indicates the size of the prefetch (read-ahead) buffer. (Get)
helpviewer_keywords: ["IFaxIncomingMessageIterator interface [Fax Service]","PrefetchSize property","IFaxIncomingMessageIterator.PrefetchSize","IFaxIncomingMessageIterator.get_PrefetchSize","IFaxIncomingMessageIterator::PrefetchSize","IFaxIncomingMessageIterator::get_PrefetchSize","IFaxIncomingMessageIterator::put_PrefetchSize","PrefetchSize property [Fax Service]","PrefetchSize property [Fax Service]","IFaxIncomingMessageIterator interface","_mfax_faxincomingmessageiterator.prefetchsize_cpp","fax._mfax_faxincomingmessageiterator_prefetchsize_cpp","faxcomex/IFaxIncomingMessageIterator::PrefetchSize","faxcomex/IFaxIncomingMessageIterator::get_PrefetchSize","faxcomex/IFaxIncomingMessageIterator::put_PrefetchSize","get_PrefetchSize"]
old-location: fax\_mfax_faxincomingmessageiterator_prefetchsize_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_64th_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessageIterator interface [Fax Service],PrefetchSize property, IFaxIncomingMessageIterator.PrefetchSize, IFaxIncomingMessageIterator.get_PrefetchSize, IFaxIncomingMessageIterator::PrefetchSize, IFaxIncomingMessageIterator::get_PrefetchSize, IFaxIncomingMessageIterator::put_PrefetchSize, PrefetchSize property [Fax Service], PrefetchSize property [Fax Service],IFaxIncomingMessageIterator interface, _mfax_faxincomingmessageiterator.prefetchsize_cpp, fax._mfax_faxincomingmessageiterator_prefetchsize_cpp, faxcomex/IFaxIncomingMessageIterator::PrefetchSize, faxcomex/IFaxIncomingMessageIterator::get_PrefetchSize, faxcomex/IFaxIncomingMessageIterator::put_PrefetchSize, get_PrefetchSize
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
 - IFaxIncomingMessageIterator::get_PrefetchSize
 - faxcomex/IFaxIncomingMessageIterator::get_PrefetchSize
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
 - IFaxIncomingMessageIterator.PrefetchSize
 - IFaxIncomingMessageIterator.get_PrefetchSize
 - IFaxIncomingMessageIterator.put_PrefetchSize
---

# IFaxIncomingMessageIterator::get_PrefetchSize


## -description

The <b>PrefetchSize</b> property indicates the size of the prefetch (read-ahead) buffer.

This property is read/write.

## -parameters

## -remarks

The prefetch buffer contains messages and makes the iteration process more efficient because you iterate through the buffer rather than through a folder. 

Changes you make to the size of the prefetch buffer take place immediately because <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator">FaxIncomingMessageIterator</a> is a local object.

The value of the <i>lPrefetchSize</i> property determines how many fax messages the iterator object retrieves from the archive each time the object refreshes its contents. The default value is <a href="/previous-versions/windows/desktop/fax/-mfax-ldefault-prefetch-size">lDEFAULT_PREFETCH_SIZE</a>.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_IN_ARCHIVE</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator-prefetchsize">PrefetchSize</a>
