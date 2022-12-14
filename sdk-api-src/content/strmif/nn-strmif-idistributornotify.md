---
UID: NN:strmif.IDistributorNotify
title: IDistributorNotify (strmif.h)
description: The IDistributorNotify interface enables a plug-in distributor to be notified when the filter graph changes.Applications never use this interface.
helpviewer_keywords: ["IDistributorNotify","IDistributorNotify interface [DirectShow]","IDistributorNotify interface [DirectShow]","described","IDistributorNotifyInterface","dshow.idistributornotify","strmif/IDistributorNotify"]
old-location: dshow\idistributornotify.htm
tech.root: dshow
ms.assetid: c7c9ee95-9d68-45c5-a3ca-8d6071782851
ms.date: 12/05/2018
ms.keywords: IDistributorNotify, IDistributorNotify interface [DirectShow], IDistributorNotify interface [DirectShow],described, IDistributorNotifyInterface, dshow.idistributornotify, strmif/IDistributorNotify
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDistributorNotify
 - strmif/IDistributorNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDistributorNotify
---

# IDistributorNotify interface


## -description

The <code>IDistributorNotify</code> interface enables a plug-in distributor to be notified when the filter graph changes.

Applications never use this interface. Implement this interface if you are writing a plug-in distributor (PID) and want the PID to receive notifications of control and changes in the composition of filter graphs.

The Filter Graph Manager queries for this interface on any plug-in distributors that it aggregates. If a PID exposes this interface, the Filter Graph Manager notifies the PID of any state changes by calling <b>IDistributorNotify</b> methods before calling the equivalent <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> methods on the filters. The Filter Graph Manager also calls the <a href="/windows/desktop/api/strmif/nf-strmif-idistributornotify-notifygraphchange">IDistributorNotify::NotifyGraphChange</a> method whenever it adds or removes a filter, or any pin connections change.

During a call to any <b>IDistributorNotify</b> method, do not hold any critical section that might be held by another code path that calls methods on the Filter Graph Manager. Doing so could result in a deadlock.

## -inheritance

The <b>IDistributorNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDistributorNotify</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/plug-in-distributors">Plug-in Distributors</a>
