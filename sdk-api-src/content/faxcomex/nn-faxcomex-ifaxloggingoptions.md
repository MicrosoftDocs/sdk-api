---
UID: NN:faxcomex.IFaxLoggingOptions
title: IFaxLoggingOptions (faxcomex.h)
description: The IFaxLoggingOptions interface is used by a fax client application to access and configure the event logging categories and the activity logging options that the fax service is using.
helpviewer_keywords: ["IFaxLoggingOptions","IFaxLoggingOptions interface [Fax Service]","IFaxLoggingOptions interface [Fax Service]","described","_mfax_faxloggingoptions_cpp","fax._mfax_faxloggingoptions_cpp","faxcomex/IFaxLoggingOptions"]
old-location: fax\_mfax_faxloggingoptions_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_70c3_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxLoggingOptions, IFaxLoggingOptions interface [Fax Service], IFaxLoggingOptions interface [Fax Service],described, _mfax_faxloggingoptions_cpp, fax._mfax_faxloggingoptions_cpp, faxcomex/IFaxLoggingOptions
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
 - IFaxLoggingOptions
 - faxcomex/IFaxLoggingOptions
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
 - IFaxLoggingOptions
---

# IFaxLoggingOptions interface


## -description

The <b>IFaxLoggingOptions</b> interface is used by a fax client application to access and configure the event logging categories and the activity logging options that the fax service is using.

The <b>IFaxLoggingOptions</b> interface is accessed through an <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a> interface. It provides access to the <a href="/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-faxeventlogging">FaxEventLogging</a> methods.

## -remarks

To create a <b>FaxLoggingOptions</b> object in C++, call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-loggingoptions">LoggingOptions</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxloggingoptions">FaxLoggingOptions</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>