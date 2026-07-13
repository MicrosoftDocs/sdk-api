---
UID: NN:faxcomex.IFaxActivityLogging
title: IFaxActivityLogging (faxcomex.h)
description: The IFaxActivityLogging interface defines a configuration object used by a fax client application to retrieve and set options for activity logging.
helpviewer_keywords: ["IFaxActivityLogging","IFaxActivityLogging interface [Fax Service]","IFaxActivityLogging interface [Fax Service]","described","_mfax_faxactivitylogging_cpp","fax._mfax_faxactivitylogging_cpp","faxcomex/IFaxActivityLogging"]
old-location: fax\_mfax_faxactivitylogging_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0odj_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxActivityLogging, IFaxActivityLogging interface [Fax Service], IFaxActivityLogging interface [Fax Service],described, _mfax_faxactivitylogging_cpp, fax._mfax_faxactivitylogging_cpp, faxcomex/IFaxActivityLogging
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
 - IFaxActivityLogging
 - faxcomex/IFaxActivityLogging
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
 - IFaxActivityLogging
---

# IFaxActivityLogging interface


## -description

The <b>IFaxActivityLogging</b> interface defines a configuration object used by a fax client application to retrieve and set options for activity logging. This includes setting whether entries for incoming and outgoing faxes should be logged and the location of the log file.

## -inheritance

The <b>IFaxActivityLogging</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxActivityLogging</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxActivityLogging</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a> object.
