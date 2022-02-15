---
UID: NF:faxcomex.IFaxOutgoingArchive.GetMessage
title: IFaxOutgoingArchive::GetMessage (faxcomex.h)
description: The IFaxOutgoingArchive::GetMessage method returns a fax message from the archive of outbound faxes by using the fax message ID.
helpviewer_keywords: ["GetMessage","GetMessage method [Fax Service]","GetMessage method [Fax Service]","IFaxOutgoingArchive interface","IFaxOutgoingArchive interface [Fax Service]","GetMessage method","IFaxOutgoingArchive.GetMessage","IFaxOutgoingArchive::GetMessage","_mfax_faxoutgoingarchive.getmessage_cpp","fax._mfax_faxoutgoingarchive_getmessage_cpp","faxcomex/IFaxOutgoingArchive::GetMessage"]
old-location: fax\_mfax_faxoutgoingarchive_getmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7did_cpp.htm
ms.date: 12/05/2018
ms.keywords: GetMessage, GetMessage method [Fax Service], GetMessage method [Fax Service],IFaxOutgoingArchive interface, IFaxOutgoingArchive interface [Fax Service],GetMessage method, IFaxOutgoingArchive.GetMessage, IFaxOutgoingArchive::GetMessage, _mfax_faxoutgoingarchive.getmessage_cpp, fax._mfax_faxoutgoingarchive_getmessage_cpp, faxcomex/IFaxOutgoingArchive::GetMessage
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
 - IFaxOutgoingArchive::GetMessage
 - faxcomex/IFaxOutgoingArchive::GetMessage
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
 - IFaxOutgoingArchive.GetMessage
---

# IFaxOutgoingArchive::GetMessage


## -description

The <b>IFaxOutgoingArchive::GetMessage</b> method returns a fax message from the archive of outbound faxes by using the fax message ID.

## -parameters

### -param bstrMessageId

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the message ID of the fax to retrieve from the archive of outbound faxes.

### -param pFaxOutgoingMessage [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a>**</b>

Address of a pointer that receives a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> or <b>farQUERY_OUT_ARCHIVE</b> access right. With the <b>farSUBMIT_LOW</b> access right, the user will be able to use this method only for his own faxes. With the <b>farQUERY_OUT_ARCHIVE</b> access right, he will be able to use this method for all of the faxes on the server.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-outgoing-archive">Visual Basic Example</a>