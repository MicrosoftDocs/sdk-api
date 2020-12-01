---
UID: NF:prnasnot.IPrintAsyncNotifyDataObject.AcquireData
title: IPrintAsyncNotifyDataObject::AcquireData (prnasnot.h)
description: Directs listening applications to the notification data, including the data's size and type.
helpviewer_keywords: ["AcquireData","AcquireData method [Windows GDI]","AcquireData method [Windows GDI]","IPrintAsyncNotifyDataObject interface","IPrintAsyncNotifyDataObject interface [Windows GDI]","AcquireData method","IPrintAsyncNotifyDataObject.AcquireData","IPrintAsyncNotifyDataObject::AcquireData","_win32_IPrintAsyncNotifyDataObject_AcquireData","gdi.iprintasyncnotifydataobject_iprintasyncnotifydataobject__acquiredata","prnasnot/IPrintAsyncNotifyDataObject::AcquireData"]
old-location: gdi\iprintasyncnotifydataobject_iprintasyncnotifydataobject__acquiredata.htm
tech.root: xps
ms.assetid: c6272583-6907-4c9f-b0c8-4d788e0b2173
ms.date: 12/05/2018
ms.keywords: AcquireData, AcquireData method [Windows GDI], AcquireData method [Windows GDI],IPrintAsyncNotifyDataObject interface, IPrintAsyncNotifyDataObject interface [Windows GDI],AcquireData method, IPrintAsyncNotifyDataObject.AcquireData, IPrintAsyncNotifyDataObject::AcquireData, _win32_IPrintAsyncNotifyDataObject_AcquireData, gdi.iprintasyncnotifydataobject_iprintasyncnotifydataobject__acquiredata, prnasnot/IPrintAsyncNotifyDataObject::AcquireData
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
req.dll: Prnasnot.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrintAsyncNotifyDataObject::AcquireData
 - prnasnot/IPrintAsyncNotifyDataObject::AcquireData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.dll
api_name:
 - IPrintAsyncNotifyDataObject.AcquireData
---

# IPrintAsyncNotifyDataObject::AcquireData


## -description

Directs listening applications to the notification data, including the data's size and type.

## -parameters

### -param ppNotificationData [out]

A buffer containing the notification data.

### -param pSize [out]

The size of the data buffer.

### -param ppSchema [out]

A GUID pointer to the data schema.

## -returns

See <a href="/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror">PrintAsyncNotifyError</a> for the possible values.

For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

## -remarks

Applications that call this method must call <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata">ReleaseData</a> when they have finished consuming the notification data.

The <a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject">IPrintAsyncNotifyDataObject</a> interface must be implemented to ensure that a call of <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> does not free the object if a listening application has not finished consuming the object's data. Accordingly, if a call to <b>Release</b> occurs when an application has called <b>AcquireData</b> but has not yet called <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata">ReleaseData</a> , then the object must not be freed. For this reason, we recommend that <b>AcquireData</b> use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> to increment the object's reference count and that <b>ReleaseData</b> decrement the count.

When the Print Spooler fails, it creates an <a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject">IPrintAsyncNotifyDataObject</a> object. When a listener calls <b>AcquireData</b> for this notification, <i>ppNotificationData</i> is <b>NULL</b>, the size is 0, and <i>ppSchema</i> is NOTIFICATION_RELEASE.

## -see-also

<a href="/windows/desktop/printdocs/asynchronous-notification-interfaces">Asynchronous Printing Notification Interfaces</a>



<a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject">IPrintAsyncNotifyDataObject</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>