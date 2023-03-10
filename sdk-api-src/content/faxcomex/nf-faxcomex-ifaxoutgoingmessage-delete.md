---
UID: NF:faxcomex.IFaxOutgoingMessage.Delete
title: IFaxOutgoingMessage::Delete (faxcomex.h)
description: The IFaxOutgoingMessage::Delete method deletes the fax message from the outbound archive.
helpviewer_keywords: ["Delete","Delete method [Fax Service]","Delete method [Fax Service]","IFaxOutgoingMessage interface","IFaxOutgoingMessage interface [Fax Service]","Delete method","IFaxOutgoingMessage.Delete","IFaxOutgoingMessage::Delete","_mfax_faxoutgoingmessage.delete","fax._mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_delete_cpp","fax._mfax_faxoutgoingmessage_delete","faxcomex/IFaxOutgoingMessage::Delete"]
old-location: fax\_mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_delete_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_06w5.htm
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Fax Service], Delete method [Fax Service],IFaxOutgoingMessage interface, IFaxOutgoingMessage interface [Fax Service],Delete method, IFaxOutgoingMessage.Delete, IFaxOutgoingMessage::Delete, _mfax_faxoutgoingmessage.delete, fax._mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_delete_cpp, fax._mfax_faxoutgoingmessage_delete, faxcomex/IFaxOutgoingMessage::Delete
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
 - IFaxOutgoingMessage::Delete
 - faxcomex/IFaxOutgoingMessage::Delete
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
 - IFaxOutgoingMessage.Delete
 - IFaxOutgoingMessage.Delete
---

# IFaxOutgoingMessage::Delete


## -description

The <b>IFaxOutgoingMessage::Delete</b> method deletes the fax message from the outbound archive.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> or <b>farMANAGE_OUT_ARCHIVE</b> access right.

With the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> access right, users will be able to use this method only for their own faxes. With the <b>farMANAGE_OUT_ARCHIVE</b> access right, users will be able to use this method for all faxes on the server.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-outgoing-archive">Visual Basic Example</a>
