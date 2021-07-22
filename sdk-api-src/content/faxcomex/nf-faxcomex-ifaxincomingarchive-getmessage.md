---
UID: NF:faxcomex.IFaxIncomingArchive.GetMessage
title: IFaxIncomingArchive::GetMessage (faxcomex.h)
description: The GetMessage method returns a fax message from the archive of inbound faxes by using the fax message ID.
helpviewer_keywords: ["GetMessage","GetMessage method [Fax Service]","GetMessage method [Fax Service]","IFaxIncomingArchive interface","IFaxIncomingArchive interface [Fax Service]","GetMessage method","IFaxIncomingArchive.GetMessage","IFaxIncomingArchive::GetMessage","_mfax_faxincomingarchive.getmessage","fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_getmessage_cpp","fax._mfax_faxincomingarchive_getmessage","faxcomex/IFaxIncomingArchive::GetMessage"]
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_getmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_223p.htm
ms.date: 12/05/2018
ms.keywords: GetMessage, GetMessage method [Fax Service], GetMessage method [Fax Service],IFaxIncomingArchive interface, IFaxIncomingArchive interface [Fax Service],GetMessage method, IFaxIncomingArchive.GetMessage, IFaxIncomingArchive::GetMessage, _mfax_faxincomingarchive.getmessage, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_getmessage_cpp, fax._mfax_faxincomingarchive_getmessage, faxcomex/IFaxIncomingArchive::GetMessage
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
 - IFaxIncomingArchive::GetMessage
 - faxcomex/IFaxIncomingArchive::GetMessage
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
 - IFaxIncomingArchive.GetMessage
 - IFaxIncomingArchive.GetMessage
---

# IFaxIncomingArchive::GetMessage


## -description

The <b>GetMessage</b> method returns a fax message from the archive of inbound faxes by using the fax message ID.

## -parameters

### -param bstrMessageId [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the message ID of the fax to retrieve from the archive of inbound faxes.

### -param pFaxIncomingMessage [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage">IFaxIncomingMessage</a>**</b>

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_IN_ARCHIVE</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>