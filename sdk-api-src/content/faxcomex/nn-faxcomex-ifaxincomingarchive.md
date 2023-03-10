---
UID: NN:faxcomex.IFaxIncomingArchive
title: IFaxIncomingArchive (faxcomex.h)
description: The IFaxIncomingArchive interface is used by a fax client application to access and configure the archive of inbound fax messages received successfully by the fax service.
helpviewer_keywords: ["IFaxIncomingArchive","IFaxIncomingArchive interface [Fax Service]","IFaxIncomingArchive interface [Fax Service]","described","_mfax_faxincomingarchive_cpp","fax._mfax_faxincomingarchive_cpp","faxcomex/IFaxIncomingArchive"]
old-location: fax\_mfax_faxincomingarchive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_96jp_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingArchive, IFaxIncomingArchive interface [Fax Service], IFaxIncomingArchive interface [Fax Service],described, _mfax_faxincomingarchive_cpp, fax._mfax_faxincomingarchive_cpp, faxcomex/IFaxIncomingArchive
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
 - IFaxIncomingArchive
 - faxcomex/IFaxIncomingArchive
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
 - IFaxIncomingArchive
---

# IFaxIncomingArchive interface


## -description

The <b>IFaxIncomingArchive</b> interface is used by a fax client application to access and configure the archive of inbound fax messages received successfully by the fax service. Use this interface to set and retrieve parameters related to configuring the archive of sent faxes. You can also use the <b>IFaxIncomingArchive</b> interface to retrieve a message from the archive by specifying its message ID.

A default implementation of <b>IFaxIncomingArchive</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a> object.

## -inheritance

The <b>IFaxIncomingArchive</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxIncomingArchive</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
