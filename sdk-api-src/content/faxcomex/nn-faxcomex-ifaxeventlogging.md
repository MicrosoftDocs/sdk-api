---
UID: NN:faxcomex.IFaxEventLogging
title: IFaxEventLogging (faxcomex.h)
description: The IFaxEventLogging interface defines a configuration object used by a fax client application to configure the event logging categories used by the fax service.
helpviewer_keywords: ["IFaxEventLogging","IFaxEventLogging interface [Fax Service]","IFaxEventLogging interface [Fax Service]","described","_mfax_faxeventlogging_cpp","fax._mfax_faxeventlogging_cpp","faxcomex/IFaxEventLogging"]
old-location: fax\_mfax_faxeventlogging_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1xt3_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxEventLogging, IFaxEventLogging interface [Fax Service], IFaxEventLogging interface [Fax Service],described, _mfax_faxeventlogging_cpp, fax._mfax_faxeventlogging_cpp, faxcomex/IFaxEventLogging
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
 - IFaxEventLogging
 - faxcomex/IFaxEventLogging
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
 - IFaxEventLogging
---

# IFaxEventLogging interface


## -description

The <b>IFaxEventLogging</b> interface defines a configuration object used by a fax client application to configure the event logging categories used by the fax service. You can specify the level of detail at which the fax service logs events in the application log.

## -inheritance

The <b>IFaxEventLogging</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxEventLogging</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxEventLogging</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxeventlogging">FaxEventLogging</a> object.
