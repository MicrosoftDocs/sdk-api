---
UID: NN:prnasnot.IPrintAsyncNotifyDataObject
title: IPrintAsyncNotifyDataObject (prnasnot.h)
description: Encapsulates the data sent in a notification channel.
helpviewer_keywords: ["IPrintAsyncNotifyDataObject","IPrintAsyncNotifyDataObject interface [Windows GDI]","IPrintAsyncNotifyDataObject interface [Windows GDI]","described","_win32_IPrintAsyncNotifyDataObject","gdi.iprintasyncnotifydataobject","prnasnot/IPrintAsyncNotifyDataObject"]
old-location: gdi\iprintasyncnotifydataobject.htm
tech.root: xps
ms.assetid: fd0e1f30-c54e-418c-8081-664edebaad61
ms.date: 12/05/2018
ms.keywords: IPrintAsyncNotifyDataObject, IPrintAsyncNotifyDataObject interface [Windows GDI], IPrintAsyncNotifyDataObject interface [Windows GDI],described, _win32_IPrintAsyncNotifyDataObject, gdi.iprintasyncnotifydataobject, prnasnot/IPrintAsyncNotifyDataObject
req.header: prnasnot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrintAsyncNotifyDataObject
 - prnasnot/IPrintAsyncNotifyDataObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.h
api_name:
 - IPrintAsyncNotifyDataObject
---

# IPrintAsyncNotifyDataObject interface


## -description

Encapsulates the data sent in a notification channel.

## -inheritance

The <b>IPrintAsyncNotifyDataObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPrintAsyncNotifyDataObject</b> also has these types of members:

## -remarks

Listening applications must call <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata">ReleaseData</a> when they have finished consuming the notification data obtained with <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata">AcquireData</a>.

The <b>IPrintAsyncNotifyDataObject</b> interface must be implemented in a way that ensures that a call of <a href="/previous-versions/dd757102(v=vs.85)">IUnknown::Release</a> does not free the object if a listening application has not finished consuming the object's data. Accordingly, if a call to <b>Release</b> occurs when an application has called <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata">AcquireData</a> but has not yet called <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata">ReleaseData</a> , then the object must not be freed. For this reason, we recommend that <b>AcquireData</b> use <a href="/previous-versions/dd757100(v=vs.85)">IUnknown::AddRef</a> to increment the object's reference count and that <b>ReleaseData</b> decrement the count.

Listening applications can live within the Print Spooler's process as well as outside it. When the listener is outside of this process, it can access only the <b>IPrintAsyncNotifyDataObject</b> methods. Hence, if your <b>IPrintAsyncNotifyDataObject</b> also implements an interface of your own, be aware that your interface's methods are available only to listening applications within the Print Spooler's process.

## -see-also

<a href="/windows/desktop/printdocs/asynchronous-notification-interfaces">Asynchronous Printing Notification Interfaces</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>
