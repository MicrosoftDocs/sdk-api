---
UID: NF:faxcomex.IFaxAccountOutgoingArchive.GetMessage
title: IFaxAccountOutgoingArchive::GetMessage (faxcomex.h)
description: Returns a fax message from the archive of outbound faxes for a particular fax account, by using the fax message ID.
helpviewer_keywords: ["GetMessage","GetMessage method [Fax Service]","GetMessage method [Fax Service]","IFaxAccountOutgoingArchive interface","IFaxAccountOutgoingArchive interface [Fax Service]","GetMessage method","IFaxAccountOutgoingArchive.GetMessage","IFaxAccountOutgoingArchive::GetMessage","_mfax_faxaccountoutgoingarchive.getmessage","fax._mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_getmessage_cpp","fax._mfax_faxaccountoutgoingarchive_getmessage","faxcomex/IFaxAccountOutgoingArchive::GetMessage"]
old-location: fax\_mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_getmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingarchive\getmessage.htm
ms.date: 12/05/2018
ms.keywords: GetMessage, GetMessage method [Fax Service], GetMessage method [Fax Service],IFaxAccountOutgoingArchive interface, IFaxAccountOutgoingArchive interface [Fax Service],GetMessage method, IFaxAccountOutgoingArchive.GetMessage, IFaxAccountOutgoingArchive::GetMessage, _mfax_faxaccountoutgoingarchive.getmessage, fax._mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_getmessage_cpp, fax._mfax_faxaccountoutgoingarchive_getmessage, faxcomex/IFaxAccountOutgoingArchive::GetMessage
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
 - IFaxAccountOutgoingArchive::GetMessage
 - faxcomex/IFaxAccountOutgoingArchive::GetMessage
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
 - IFaxAccountOutgoingArchive.GetMessage
 - IFaxAccountOutgoingArchive.GetMessage
---

# IFaxAccountOutgoingArchive::GetMessage


## -description

Returns a fax message from the archive of outbound faxes for a particular fax account, by using the fax message ID.

## -parameters

### -param bstrMessageId [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the message ID of the fax to retrieve from the archive of outbound faxes.

### -param pFaxOutgoingMessage

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a>**</b>

A <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountoutgoingarchive">FaxAccountOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountoutgoingarchive">IFaxAccountOutgoingArchive</a>