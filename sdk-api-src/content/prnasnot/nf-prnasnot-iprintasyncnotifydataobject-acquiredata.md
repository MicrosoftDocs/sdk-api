---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.




## -remarks



Applications that call this method must call <a href="https://msdn.microsoft.com/f4960aa1-237f-491e-b69c-0aa107d9ddad">ReleaseData</a> when they have finished consuming the notification data.

The <a href="https://msdn.microsoft.com/fd0e1f30-c54e-418c-8081-664edebaad61">IPrintAsyncNotifyDataObject</a> interface must be implemented to ensure that a call of <a href="_com_iunknown_release">IUnknown::Release</a> does not free the object if a listening application has not finished consuming the object's data. Accordingly, if a call to <b>Release</b> occurs when an application has called <b>AcquireData</b> but has not yet called <a href="https://msdn.microsoft.com/f4960aa1-237f-491e-b69c-0aa107d9ddad">ReleaseData</a> , then the object must not be freed. For this reason, we recommend that <b>AcquireData</b> use <a href="_com_iunknown_addref">IUnknown::AddRef</a> to increment the object's reference count and that <b>ReleaseData</b> decrement the count.

When the Print Spooler fails, it creates an <a href="https://msdn.microsoft.com/fd0e1f30-c54e-418c-8081-664edebaad61">IPrintAsyncNotifyDataObject</a> object. When a listener calls <b>AcquireData</b> for this notification, <i>ppNotificationData</i> is <b>NULL</b>, the size is 0, and <i>ppSchema</i> is NOTIFICATION_RELEASE.




## -see-also




<a href="https://msdn.microsoft.com/e96c957f-3972-4afc-9d76-a4725b8688f8">Asynchronous Printing Notification Interfaces</a>



<a href="https://msdn.microsoft.com/fd0e1f30-c54e-418c-8081-664edebaad61">IPrintAsyncNotifyDataObject</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

