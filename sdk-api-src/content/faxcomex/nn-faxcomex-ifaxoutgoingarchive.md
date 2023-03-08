---
UID: NN:faxcomex.IFaxOutgoingArchive
title: IFaxOutgoingArchive (faxcomex.h)
description: The IFaxOutgoingArchive interface describes a configuration object that is used by a fax client application to access and configure the archive of outbound fax messages transmitted successfully by the fax service.
helpviewer_keywords: ["IFaxOutgoingArchive","IFaxOutgoingArchive interface [Fax Service]","IFaxOutgoingArchive interface [Fax Service]","described","_mfax_faxoutgoingarchive_cpp","fax._mfax_faxoutgoingarchive_cpp","faxcomex/IFaxOutgoingArchive"]
old-location: fax\_mfax_faxoutgoingarchive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_3wmd_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingArchive, IFaxOutgoingArchive interface [Fax Service], IFaxOutgoingArchive interface [Fax Service],described, _mfax_faxoutgoingarchive_cpp, fax._mfax_faxoutgoingarchive_cpp, faxcomex/IFaxOutgoingArchive
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
 - IFaxOutgoingArchive
 - faxcomex/IFaxOutgoingArchive
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
 - IFaxOutgoingArchive
---

# IFaxOutgoingArchive interface


## -description

The <b>IFaxOutgoingArchive</b> interface describes a configuration object that is used by a fax client application to access and configure the archive of outbound fax messages transmitted successfully by the fax service. You can also use the <b>IFaxOutgoingArchive</b> interface to retrieve a message from the archive using its message ID.

## -inheritance

The <b>IFaxOutgoingArchive</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutgoingArchive</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxOutgoingArchive</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a> object.
