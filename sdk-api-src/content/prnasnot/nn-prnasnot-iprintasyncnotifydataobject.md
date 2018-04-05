---
UID: NN:prnasnot.IPrintAsyncNotifyDataObject
title: IPrintAsyncNotifyDataObject
author: windows-driver-content
description: Encapsulates the data sent in a notification channel.
old-location: gdi\iprintasyncnotifydataobject.htm
old-project: printdocs
ms.assetid: fd0e1f30-c54e-418c-8081-664edebaad61
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IPrintAsyncNotifyDataObject, IPrintAsyncNotifyDataObject interface [Windows GDI], IPrintAsyncNotifyDataObject interface [Windows GDI], described, _win32_IPrintAsyncNotifyDataObject, gdi.iprintasyncnotifydataobject, prnasnot/IPrintAsyncNotifyDataObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: PrintAsyncNotifyUserFilter
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	prnasnot.h
api_name:
-	IPrintAsyncNotifyDataObject
product: Windows
targetos: Windows
req.lib: WinSpool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPrintAsyncNotifyDataObject interface


## -description


Encapsulates the data sent in a notification channel. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintAsyncNotifyDataObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPrintAsyncNotifyDataObject</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c6272583-6907-4c9f-b0c8-4d788e0b2173">AcquireData</a>
</td>
<td align="left" width="63%">
Provides encapsulated notification data to listening applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4960aa1-237f-491e-b69c-0aa107d9ddad">ReleaseData</a>
</td>
<td align="left" width="63%">
Enables a listening application to release the notification data after it has been consumed.

</td>
</tr>
</table> 


## -remarks



Listening applications must call <a href="https://msdn.microsoft.com/f4960aa1-237f-491e-b69c-0aa107d9ddad">ReleaseData</a> when they have finished consuming the notification data obtained with <a href="https://msdn.microsoft.com/c6272583-6907-4c9f-b0c8-4d788e0b2173">AcquireData</a>.

The <b>IPrintAsyncNotifyDataObject</b> interface must be implemented in a way that ensures that a call of <a href="https://msdn.microsoft.com/61d760e3-72bf-462e-bfd5-5578b53860ba">IUnknown::Release</a> does not free the object if a listening application has not finished consuming the object's data. Accordingly, if a call to <b>Release</b> occurs when an application has called <a href="https://msdn.microsoft.com/c6272583-6907-4c9f-b0c8-4d788e0b2173">AcquireData</a> but has not yet called <a href="https://msdn.microsoft.com/f4960aa1-237f-491e-b69c-0aa107d9ddad">ReleaseData</a> , then the object must not be freed. For this reason, we recommend that <b>AcquireData</b> use <a href="https://msdn.microsoft.com/14ffd2ab-ac0c-4de7-adb8-4fe800c9bda9">IUnknown::AddRef</a> to increment the object's reference count and that <b>ReleaseData</b> decrement the count.

Listening applications can live within the Print Spooler's process as well as outside it. When the listener is outside of this process, it can access only the <b>IPrintAsyncNotifyDataObject</b> methods. Hence, if your <b>IPrintAsyncNotifyDataObject</b> also implements an interface of your own, be aware that your interface's methods are available only to listening applications within the Print Spooler's process.




## -see-also




<a href="https://msdn.microsoft.com/e96c957f-3972-4afc-9d76-a4725b8688f8">Asynchronous Printing Notification Interfaces</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

