---
UID: NF:faxcomex.IFaxOutgoingArchive.GetMessages
title: IFaxOutgoingArchive::GetMessages (faxcomex.h)
description: The IFaxOutgoingArchive::GetMessages method returns a new iterator (archive cursor) for the archive of outbound fax messages. For more information, see IFaxOutgoingMessageIterator.
helpviewer_keywords: ["GetMessages","GetMessages method [Fax Service]","GetMessages method [Fax Service]","IFaxOutgoingArchive interface","IFaxOutgoingArchive interface [Fax Service]","GetMessages method","IFaxOutgoingArchive.GetMessages","IFaxOutgoingArchive::GetMessages","_mfax_faxoutgoingarchive.getmessages_cpp","fax._mfax_faxoutgoingarchive_getmessages_cpp","faxcomex/IFaxOutgoingArchive::GetMessages"]
old-location: fax\_mfax_faxoutgoingarchive_getmessages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_20qb_cpp.htm
ms.date: 12/05/2018
ms.keywords: GetMessages, GetMessages method [Fax Service], GetMessages method [Fax Service],IFaxOutgoingArchive interface, IFaxOutgoingArchive interface [Fax Service],GetMessages method, IFaxOutgoingArchive.GetMessages, IFaxOutgoingArchive::GetMessages, _mfax_faxoutgoingarchive.getmessages_cpp, fax._mfax_faxoutgoingarchive_getmessages_cpp, faxcomex/IFaxOutgoingArchive::GetMessages
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
 - IFaxOutgoingArchive::GetMessages
 - faxcomex/IFaxOutgoingArchive::GetMessages
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
 - IFaxOutgoingArchive.GetMessages
---

# IFaxOutgoingArchive::GetMessages


## -description

The <b>IFaxOutgoingArchive::GetMessages</b> method returns a new iterator (archive cursor) for the archive of outbound fax messages. For more information, see <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a>.

## -parameters

### -param lPrefetchSize

Type: <b>long</b>

A <b>long</b> value that specifies the size of the prefetch buffer. This value determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents. The default value is <a href="/previous-versions/windows/desktop/fax/-mfax-ldefault-prefetch-size">lDEFAULT_PREFETCH_SIZE</a>.

### -param pFaxOutgoingMessageIterator [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a>**</b>

An address of a pointer that receives the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> or <b>farQUERY_OUT_ARCHIVE</b> access right. With the <b>farSUBMIT_LOW</b> access right, the user will be able to use this method only for his own faxes. With the <b>farQUERY_OUT_ARCHIVE</b> access right, he will be able to use this method for all of the faxes on the server.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-outgoing-archive">Visual Basic Example</a>