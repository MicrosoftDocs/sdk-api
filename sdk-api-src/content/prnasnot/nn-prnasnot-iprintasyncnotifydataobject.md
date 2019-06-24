---
UID: NN:prnasnot.IPrintAsyncNotifyDataObject
title: IPrintAsyncNotifyDataObject (prnasnot.h)
author: windows-sdk-content
description: Encapsulates the data sent in a notification channel.
old-location: gdi\iprintasyncnotifydataobject.htm
tech.root: printdocs
ms.assetid: fd0e1f30-c54e-418c-8081-664edebaad61
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPrintAsyncNotifyDataObject, IPrintAsyncNotifyDataObject interface [Windows GDI], IPrintAsyncNotifyDataObject interface [Windows GDI],described, _win32_IPrintAsyncNotifyDataObject, gdi.iprintasyncnotifydataobject, prnasnot/IPrintAsyncNotifyDataObject
ms.topic: interface
f1_keywords: ["prnasnot/IPrintAsyncNotifyDataObject"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.h
api_name:
 - IPrintAsyncNotifyDataObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPrintAsyncNotifyDataObject interface


## -description


Encapsulates the data sent in a notification channel. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintAsyncNotifyDataObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPrintAsyncNotifyDataObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintAsyncNotifyDataObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata">AcquireData</a>
</td>
<td align="left" width="63%">
Provides encapsulated notification data to listening applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata">ReleaseData</a>
</td>
<td align="left" width="63%">
Enables a listening application to release the notification data after it has been consumed.

</td>
</tr>
</table> 


## -remarks



Listening applications must call <a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata">ReleaseData</a> when they have finished consuming the notification data obtained with <a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata">AcquireData</a>.

The <b>IPrintAsyncNotifyDataObject</b> interface must be implemented in a way that ensures that a call of <a href="https://docs.microsoft.com/previous-versions/dd757102(v=vs.85)">IUnknown::Release</a> does not free the object if a listening application has not finished consuming the object's data. Accordingly, if a call to <b>Release</b> occurs when an application has called <a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata">AcquireData</a> but has not yet called <a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata">ReleaseData</a> , then the object must not be freed. For this reason, we recommend that <b>AcquireData</b> use <a href="https://docs.microsoft.com/previous-versions/dd757100(v=vs.85)">IUnknown::AddRef</a> to increment the object's reference count and that <b>ReleaseData</b> decrement the count.

Listening applications can live within the Print Spooler's process as well as outside it. When the listener is outside of this process, it can access only the <b>IPrintAsyncNotifyDataObject</b> methods. Hence, if your <b>IPrintAsyncNotifyDataObject</b> also implements an interface of your own, be aware that your interface's methods are available only to listening applications within the Print Spooler's process.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/printdocs/asynchronous-notification-interfaces">Asynchronous Printing Notification Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/printdocs/printdocs-printing">Printing</a>
 

 

