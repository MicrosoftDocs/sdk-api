---
UID: NF:wabiab.IAddrBook.Advise
tech.root: wab wab 
title: IAddrBook::Advise
ms.date: 03/03/2021
ms.topic: language-reference
targetos: Windows
description: Registers the caller with the Windows Address Book (WAB) to receive notifications.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wabiab.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wabiab.h
api_name:
 - IAddrBook::Advise
f1_keywords:
 - IAddrBook::Advise
 - wabiab/IAddrBook::Advise
dev_langs:
 - c++
---

## -description

Registers the caller with the Windows Address Book (WAB) to receive notifications.

## -parameters

### -param cbEntryID

Reserved. Must be set to 0.

### -param lpEntryID

Reserved. Must be set to NULL.

### -param ulEventMask

Value of type ULONG that specifies the event masks. Set to **fnevObjectModified**. All other event masks will be rejected.

### -param lpAdviseSink

Pointer to an **IUnknown** interface that specifies the object invoked by the Windows Address Book (WAB) to send notifications.

### -param lpulConnection

Pointer to a variable of type ULONG that receives the connection number returned by the Windows Address Book (WAB). Use this number when calling [IAddrBook::Unadvise](nf-wabiab-iaddrbook-unadvise.md).

## -returns

HRESULT

## -remarks

At this time, the Windows Address Book (WAB) only provides notifications to generic changes in the store. Clients cannot register for notifications provided per entry identifier. When the Windows Address Book (WAB) store changes, the Windows Address Book (WAB) invokes the **IMAPIAdviseSink::OnNotify** method on the *lpAdviseSink* pointer passed into this function.

The **NOTIFICATION** structure passed to the **OnNotify method has the following valid members:

```
<![CDATA[Notification.ulEventType = fnevObjectModified
Notification.info.obj.ulObjType = MAPI_ADDRBOOK]]>
```
	
All other members in the structure will be NULL or zero. Clients must use this notification only for refreshing their UI. Detailed information about modifications to individual objects within the Windows Address Book (WAB) is not currently available.

## -see-also

