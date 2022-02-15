---
UID: NF:faxcomex.IFaxIncomingMessage.Delete
title: IFaxIncomingMessage::Delete (faxcomex.h)
description: The Delete method deletes the specified fax message from the inbound fax archive.
helpviewer_keywords: ["Delete","Delete method [Fax Service]","Delete method [Fax Service]","IFaxIncomingMessage interface","IFaxIncomingMessage interface [Fax Service]","Delete method","IFaxIncomingMessage.Delete","IFaxIncomingMessage::Delete","_mfax_faxincomingmessage.delete","fax._mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_delete_cpp","fax._mfax_faxincomingmessage_delete","faxcomex/IFaxIncomingMessage::Delete"]
old-location: fax\_mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_delete_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_025h.htm
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Fax Service], Delete method [Fax Service],IFaxIncomingMessage interface, IFaxIncomingMessage interface [Fax Service],Delete method, IFaxIncomingMessage.Delete, IFaxIncomingMessage::Delete, _mfax_faxincomingmessage.delete, fax._mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_delete_cpp, fax._mfax_faxincomingmessage_delete, faxcomex/IFaxIncomingMessage::Delete
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
 - IFaxIncomingMessage::Delete
 - faxcomex/IFaxIncomingMessage::Delete
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
 - IFaxIncomingMessage.Delete
 - IFaxIncomingMessage.Delete
---

# IFaxIncomingMessage::Delete


## -description

The <b>Delete</b> method deletes the specified fax message from the inbound fax archive.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_IN_ARCHIVE</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage">IFaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-incoming-archive">Visual Basic Example</a>
