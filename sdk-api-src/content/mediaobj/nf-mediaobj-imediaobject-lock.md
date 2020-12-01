---
UID: NF:mediaobj.IMediaObject.Lock
title: IMediaObject::Lock (mediaobj.h)
description: The Lock method acquires or releases a lock on the DMO. Call this method to keep the DMO serialized when performing multiple operations.
helpviewer_keywords: ["IMediaObject interface [DirectShow]","Lock method","IMediaObject.Lock","IMediaObject::Lock","IMediaObjectLock","Lock","Lock method [DirectShow]","Lock method [DirectShow]","IMediaObject interface","dshow.imediaobject_lock","mediaobj/IMediaObject::Lock"]
old-location: dshow\imediaobject_lock.htm
tech.root: dshow
ms.assetid: 6923dd91-7bdb-4a0c-833d-4742973825ee
ms.date: 12/05/2018
ms.keywords: IMediaObject interface [DirectShow],Lock method, IMediaObject.Lock, IMediaObject::Lock, IMediaObjectLock, Lock, Lock method [DirectShow], Lock method [DirectShow],IMediaObject interface, dshow.imediaobject_lock, mediaobj/IMediaObject::Lock
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaObject::Lock
 - mediaobj/IMediaObject::Lock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.Lock
---

# IMediaObject::Lock


## -description

The <code>Lock</code> method acquires or releases a lock on the DMO. Call this method to keep the DMO serialized when performing multiple operations.

## -parameters

### -param bLock

Value that specifies whether to acquire or release the lock. If the value is non-zero, a lock is acquired. If the value is zero, the lock is released.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

This method prevents other threads from calling methods on the DMO. If another thread calls a method on the DMO, the thread blocks until the lock is released.

If you are using the Active Template Library (ATL) to implement a DMO, the name of the Lock method conflicts with the <b>CComObjectRootEx::Lock</b> method. To work around this problem, define the preprocessor symbol FIX_LOCK_NAME before including the header file Dmo.h:


```cpp

#define FIX_LOCK_NAME
#include <dmo.h>

```


This directive causes the preprocessor to rename the <b>IMediaObject</b> method to <i>DMOLock</i>. In your DMO, implement the method as <i>DMOLock</i>. In your implementation, call the ATL <b>Lock</b> or <b>Unlock</b> method, depending on the value of <i>bLock</i>. Applications can still invoke the method using the name <i>Lock</i> because the vtable order does not change.

