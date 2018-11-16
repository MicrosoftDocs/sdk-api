---
UID: NF:prnasnot.IPrintAsyncNotifyDataObject.ReleaseData
title: IPrintAsyncNotifyDataObject::ReleaseData
author: windows-sdk-content
description: Releases the memory used by the data encapsulated in IPrintAsyncNotifyDataObject.
old-location: gdi\iprintasyncnotifydataobject_iprintasyncnotifydataobject__releasedata.htm
tech.root: printdocs
ms.assetid: f4960aa1-237f-491e-b69c-0aa107d9ddad
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IPrintAsyncNotifyDataObject interface [Windows GDI],ReleaseData method, IPrintAsyncNotifyDataObject.ReleaseData, IPrintAsyncNotifyDataObject::ReleaseData, ReleaseData, ReleaseData method [Windows GDI], ReleaseData method [Windows GDI],IPrintAsyncNotifyDataObject interface, _win32_IPrintAsyncNotifyDataObject_ReleaseData, gdi.iprintasyncnotifydataobject_iprintasyncnotifydataobject__releasedata, prnasnot/IPrintAsyncNotifyDataObject::ReleaseData
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
 - IPrintAsyncNotifyDataObject.ReleaseData
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
- IPrintAsyncNotifyDataObject.ReleaseData
: 
---

# IPrintAsyncNotifyDataObject::ReleaseData


## -description


Releases the memory used by the data encapsulated in <a href="https://msdn.microsoft.com/fd0e1f30-c54e-418c-8081-664edebaad61">IPrintAsyncNotifyDataObject</a>.


## -parameters






## -returns



See <a href="https://msdn.microsoft.com/2fb6698c-5d59-4ba0-a8ff-1313fade438c">PrintAsyncNotifyError</a> for the possible values.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa376932(v=VS.85).aspx">Error Handling</a>.




## -remarks



Listening applications must call this method when they have finished consuming the notification data.

The <a href="https://msdn.microsoft.com/fd0e1f30-c54e-418c-8081-664edebaad61">IPrintAsyncNotifyDataObject</a> interface must be implemented in a way that ensures that a call of <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> does not free the object if a listening application has not finished consuming the object's data. Accordingly, if a call to <b>Release</b> occurs when an application has called <a href="https://msdn.microsoft.com/c6272583-6907-4c9f-b0c8-4d788e0b2173">AcquireData</a> but has not yet called <b>ReleaseData</b>, then the object must not be freed. For this reason, we recommend that <b>AcquireData</b> use <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">IUnknown::AddRef</a> to increment the object's reference count, and that <b>ReleaseData</b> decrement the count.




## -see-also




<a href="https://msdn.microsoft.com/e96c957f-3972-4afc-9d76-a4725b8688f8">Asynchronous Printing Notification Interfaces</a>



<a href="https://msdn.microsoft.com/fd0e1f30-c54e-418c-8081-664edebaad61">IPrintAsyncNotifyDataObject</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

