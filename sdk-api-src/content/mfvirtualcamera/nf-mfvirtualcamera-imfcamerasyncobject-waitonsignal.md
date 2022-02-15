---
UID: NF:mfvirtualcamera.IMFCameraSyncObject.WaitOnSignal
tech.root: mf
title: IMFCameraSyncObject::WaitOnSignal
ms.date: 05/17/2021
targetos: Windows
description: Blocks until the time out specified timeout interval has elapsed or the synchronization object was signaled.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: mfsensorgroup.dll
req.header: mfvirtualcamera.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: mfsensorgroup.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - mfsensorgroup.dll
api_name:
 - IMFCameraSyncObject::WaitOnSignal
f1_keywords:
 - IMFCameraSyncObject::WaitOnSignal
 - mfvirtualcamera/IMFCameraSyncObject::WaitOnSignal
dev_langs:
 - c++
---

## -description

Blocks until the time out specified timeout interval has elapsed or the synchronization object was signaled.

## -parameters

### -param timeOutInMs

The timeout value in milliseconds.  Specifying INFINITE will result in the call blocking until the synchronization object is signaled.

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |

## -remarks

## -see-also

