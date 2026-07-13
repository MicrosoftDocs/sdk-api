---
UID: NF:faxcomex.IFaxAccountOutgoingArchive.GetMessages
title: IFaxAccountOutgoingArchive::GetMessages (faxcomex.h)
description: Returns a new iterator (archive cursor) for the archive of outbound fax messages for a particular fax account.
helpviewer_keywords: ["GetMessages","GetMessages method [Fax Service]","GetMessages method [Fax Service]","IFaxAccountOutgoingArchive interface","IFaxAccountOutgoingArchive interface [Fax Service]","GetMessages method","IFaxAccountOutgoingArchive.GetMessages","IFaxAccountOutgoingArchive::GetMessages","_mfax_faxaccountoutgoingarchive.getmessages","fax._mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_getmessages_cpp","fax._mfax_faxaccountoutgoingarchive_getmessages","faxcomex/IFaxAccountOutgoingArchive::GetMessages"]
old-location: fax\_mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_getmessages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingarchive\getmessages.htm
ms.date: 12/05/2018
ms.keywords: GetMessages, GetMessages method [Fax Service], GetMessages method [Fax Service],IFaxAccountOutgoingArchive interface, IFaxAccountOutgoingArchive interface [Fax Service],GetMessages method, IFaxAccountOutgoingArchive.GetMessages, IFaxAccountOutgoingArchive::GetMessages, _mfax_faxaccountoutgoingarchive.getmessages, fax._mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_getmessages_cpp, fax._mfax_faxaccountoutgoingarchive_getmessages, faxcomex/IFaxAccountOutgoingArchive::GetMessages
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxAccountOutgoingArchive::GetMessages
 - faxcomex/IFaxAccountOutgoingArchive::GetMessages
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
 - IFaxAccountOutgoingArchive.GetMessages
 - IFaxAccountOutgoingArchive.GetMessages
---

# IFaxAccountOutgoingArchive::GetMessages


## -description

Returns a new iterator (archive cursor) for the archive of outbound fax messages for a particular fax account.

## -parameters

### -param lPrefetchSize [in]

Type: <b>long</b>

<b>long</b> value that indicates the size of the prefetch buffer. This value determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents. The default value is <a href="/previous-versions/windows/desktop/fax/-mfax-ldefault-prefetch-size">lDEFAULT_PREFETCH_SIZE</a>.

### -param pFaxOutgoingMessageIterator

Type: <b>IFaxOutgoingMessageIterator**</b>

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator">FaxOutgoingMessageIterator</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountoutgoingarchive">FaxAccountOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator">FaxOutgoingMessageIterator</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountoutgoingarchive">IFaxAccountOutgoingArchive</a>