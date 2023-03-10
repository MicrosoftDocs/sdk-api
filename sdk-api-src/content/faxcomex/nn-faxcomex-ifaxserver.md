---
UID: NN:faxcomex.IFaxServer
title: IFaxServer (faxcomex.h)
description: The IFaxServer interface describes a messaging collection that is used by a fax client application to manage a connection to the fax service.
helpviewer_keywords: ["IFaxServer","IFaxServer interface [Fax Service]","IFaxServer interface [Fax Service]","described","_mfax_faxserver_cpp","fax._mfax_faxserver_cpp","faxcomex/IFaxServer"]
old-location: fax\_mfax_faxserver_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4isy_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer, IFaxServer interface [Fax Service], IFaxServer interface [Fax Service],described, _mfax_faxserver_cpp, fax._mfax_faxserver_cpp, faxcomex/IFaxServer
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
 - IFaxServer
 - faxcomex/IFaxServer
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
 - IFaxServer
---

# IFaxServer interface


## -description

The <b>IFaxServer</b> interface describes a messaging collection that is used by a fax client application to manage a connection to the fax service. The object includes methods to create and terminate connections with a fax server, and to retrieve information about a connected fax server. The object also includes methods to store extension configuration properties.

## -inheritance

The <b>IFaxServer</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxServer</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxServer</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a> object.
