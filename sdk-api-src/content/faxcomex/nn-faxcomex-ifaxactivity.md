---
UID: NN:faxcomex.IFaxActivity
title: IFaxActivity (faxcomex.h)
description: The IFaxActivity interface defines a read-only configuration object.
helpviewer_keywords: ["IFaxActivity","IFaxActivity interface [Fax Service]","IFaxActivity interface [Fax Service]","described","_mfax_faxactivity_cpp","fax._mfax_faxactivity_cpp","faxcomex/IFaxActivity"]
old-location: fax\_mfax_faxactivity_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4k55_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxActivity, IFaxActivity interface [Fax Service], IFaxActivity interface [Fax Service],described, _mfax_faxactivity_cpp, fax._mfax_faxactivity_cpp, faxcomex/IFaxActivity
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
 - IFaxActivity
 - faxcomex/IFaxActivity
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
 - IFaxActivity
---

# IFaxActivity interface


## -description

The <b>IFaxActivity</b> interface defines a read-only configuration object. The object permits a fax client application to access information about the activity on a connected fax server. For example, you can retrieve information about the number of outbound routing jobs that are currently executing, those that are pending processing, and those that are waiting in the job queue.

## -inheritance

The <b>IFaxActivity</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxActivity</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxActivity</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxactivity">FaxActivity</a> object.

You can configure whether the fax service logs information about incoming and outgoing fax jobs in an activity log database. The <a href="/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a> configuration object permits configuration of the activity logging options that the fax service uses.
