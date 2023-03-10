---
UID: NF:faxcomex.IFaxIncomingArchive.GetMessages
title: IFaxIncomingArchive::GetMessages (faxcomex.h)
description: The GetMessages method returns a new iterator (archive cursor) for the archive of inbound fax messages.
helpviewer_keywords: ["GetMessages","GetMessages method [Fax Service]","GetMessages method [Fax Service]","IFaxIncomingArchive interface","IFaxIncomingArchive interface [Fax Service]","GetMessages method","IFaxIncomingArchive.GetMessages","IFaxIncomingArchive::GetMessages","_mfax_faxincomingarchive.getmessages","fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_getmessages_cpp","fax._mfax_faxincomingarchive_getmessages","faxcomex/IFaxIncomingArchive::GetMessages"]
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_getmessages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1qnn.htm
ms.date: 12/05/2018
ms.keywords: GetMessages, GetMessages method [Fax Service], GetMessages method [Fax Service],IFaxIncomingArchive interface, IFaxIncomingArchive interface [Fax Service],GetMessages method, IFaxIncomingArchive.GetMessages, IFaxIncomingArchive::GetMessages, _mfax_faxincomingarchive.getmessages, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_getmessages_cpp, fax._mfax_faxincomingarchive_getmessages, faxcomex/IFaxIncomingArchive::GetMessages
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
 - IFaxIncomingArchive::GetMessages
 - faxcomex/IFaxIncomingArchive::GetMessages
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
 - IFaxIncomingArchive.GetMessages
 - IFaxIncomingArchive.GetMessages
---

# IFaxIncomingArchive::GetMessages


## -description

The <b>GetMessages</b> method returns a new iterator (archive cursor) for the archive of inbound fax messages.

## -parameters

### -param lPrefetchSize [in]

Type: <b>long</b>

<b>long</b> value that indicates the size of the prefetch buffer. This value determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents. The default value is <a href="/previous-versions/windows/desktop/fax/-mfax-ldefault-prefetch-size">lDEFAULT_PREFETCH_SIZE</a>.

### -param pFaxIncomingMessageIterator [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a>**</b>

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator">FaxIncomingMessageIterator</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_IN_ARCHIVE</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator">FaxIncomingMessageIterator</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>