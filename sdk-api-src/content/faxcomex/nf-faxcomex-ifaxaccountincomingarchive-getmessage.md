---
UID: NF:faxcomex.IFaxAccountIncomingArchive.GetMessage
title: IFaxAccountIncomingArchive::GetMessage (faxcomex.h)
description: Returns a fax message from the archive of inbound faxes, for a particular fax account, by using the fax message ID.
helpviewer_keywords: ["GetMessage","GetMessage method [Fax Service]","GetMessage method [Fax Service]","IFaxAccountIncomingArchive interface","IFaxAccountIncomingArchive interface [Fax Service]","GetMessage method","IFaxAccountIncomingArchive.GetMessage","IFaxAccountIncomingArchive::GetMessage","_mfax_faxaccountincomingarchive.getmessage","fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_getmessage_cpp","fax._mfax_faxaccountincomingarchive_getmessage","faxcomex/IFaxAccountIncomingArchive::GetMessage"]
old-location: fax\_mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_getmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingarchive\getmessage.htm
ms.date: 12/05/2018
ms.keywords: GetMessage, GetMessage method [Fax Service], GetMessage method [Fax Service],IFaxAccountIncomingArchive interface, IFaxAccountIncomingArchive interface [Fax Service],GetMessage method, IFaxAccountIncomingArchive.GetMessage, IFaxAccountIncomingArchive::GetMessage, _mfax_faxaccountincomingarchive.getmessage, fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_getmessage_cpp, fax._mfax_faxaccountincomingarchive_getmessage, faxcomex/IFaxAccountIncomingArchive::GetMessage
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
 - IFaxAccountIncomingArchive::GetMessage
 - faxcomex/IFaxAccountIncomingArchive::GetMessage
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
 - IFaxAccountIncomingArchive.GetMessage
 - IFaxAccountIncomingArchive.GetMessage
---

# IFaxAccountIncomingArchive::GetMessage


## -description

Returns a fax message from the archive of inbound faxes, for a particular fax account, by using the fax message ID.

## -parameters

### -param bstrMessageId [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the message ID of the fax to retrieve from the archive of inbound faxes.

### -param pFaxIncomingMessage

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage">IFaxIncomingMessage</a>**</b>

An <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage">IFaxIncomingMessage</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_ARCHIVES</a> access right. 

If the setting 'All incoming faxes are viewable by everyone' is true (see <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-incomingfaxesarepublic-vb">IncomingFaxesArePublic</a>) or if <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2MANAGE_RECEIVE_FOLDER</a> access rights, then the fax service searches all faxes in the Incoming archive of the Fax Server Receive Folder.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive">FaxAccountIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountincomingarchive">IFaxAccountIncomingArchive</a>