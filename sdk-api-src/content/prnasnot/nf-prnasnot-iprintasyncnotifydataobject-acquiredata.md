---
UID: NF:prnasnot.IPrintAsyncNotifyDataObject.AcquireData
title: IPrintAsyncNotifyDataObject::AcquireData
author: windows-sdk-content
description: Directs listening applications to the notification data, including the data's size and type.
old-location: gdi\iprintasyncnotifydataobject_iprintasyncnotifydataobject__acquiredata.htm
tech.root: printdocs
ms.assetid: c6272583-6907-4c9f-b0c8-4d788e0b2173
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: AcquireData, AcquireData method [Windows GDI], AcquireData method [Windows GDI],IPrintAsyncNotifyDataObject interface, IPrintAsyncNotifyDataObject interface [Windows GDI],AcquireData method, IPrintAsyncNotifyDataObject.AcquireData, IPrintAsyncNotifyDataObject::AcquireData, _win32_IPrintAsyncNotifyDataObject_AcquireData, gdi.iprintasyncnotifydataobject_iprintasyncnotifydataobject__acquiredata, prnasnot/IPrintAsyncNotifyDataObject::AcquireData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.dll
api_name:
 - IPrintAsyncNotifyDataObject.AcquireData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- prnasnot.h
: 
- IPrintAsyncNotifyDataObject.AcquireData
: 
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



See <a href="https://msdn.microsoft.com/2fb6698c-5d59-4ba0-a8ff-1313fade438c">PrintAsyncNotifyError</a> for the possible values.

For more information about COM error codes, see <a href="_com_error_handling">Error Handling</a>.




## -remarks



Applications that call this method must call <a href="https://msdn.microsoft.com/f4960aa1-237f-491e-b69c-0aa107d9ddad">ReleaseData</a> when they have finished consuming the notification data.

The <a href="https://msdn.microsoft.com/fd0e1f30-c54e-418c-8081-664edebaad61">IPrintAsyncNotifyDataObject</a> interface must be implemented to ensure that a call of <a href="_com_iunknown_release">IUnknown::Release</a> does not free the object if a listening application has not finished consuming the object's data. Accordingly, if a call to <b>Release</b> occurs when an application has called <b>AcquireData</b> but has not yet called <a href="https://msdn.microsoft.com/f4960aa1-237f-491e-b69c-0aa107d9ddad">ReleaseData</a> , then the object must not be freed. For this reason, we recommend that <b>AcquireData</b> use <a href="_com_iunknown_addref">IUnknown::AddRef</a> to increment the object's reference count and that <b>ReleaseData</b> decrement the count.

When the Print Spooler fails, it creates an <a href="https://msdn.microsoft.com/fd0e1f30-c54e-418c-8081-664edebaad61">IPrintAsyncNotifyDataObject</a> object. When a listener calls <b>AcquireData</b> for this notification, <i>ppNotificationData</i> is <b>NULL</b>, the size is 0, and <i>ppSchema</i> is NOTIFICATION_RELEASE.




## -see-also




<a href="https://msdn.microsoft.com/e96c957f-3972-4afc-9d76-a4725b8688f8">Asynchronous Printing Notification Interfaces</a>



<a href="https://msdn.microsoft.com/fd0e1f30-c54e-418c-8081-664edebaad61">IPrintAsyncNotifyDataObject</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

