---
UID: NS:projectedfslib.PRJ_CALLBACKS
title: PRJ_CALLBACKS (projectedfslib.h)
description: A set of callback routines to where the provider stores its implementation of the callback.
helpviewer_keywords: ["PRJ_CALLBACKS","PRJ_CALLBACKS structure","ProjFS.prj_callbacks","projectedfslib/PRJ_CALLBACKS"]
old-location: projfs\prj_callbacks.htm
tech.root: ProjFS
ms.assetid: 2FFF6A39-92C0-4BD1-B293-AC5650B2575C
ms.date: 12/05/2018
ms.keywords: PRJ_CALLBACKS, PRJ_CALLBACKS structure, ProjFS.prj_callbacks, projectedfslib/PRJ_CALLBACKS
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: PRJ_CALLBACKS
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_CALLBACKS
 - projectedfslib/PRJ_CALLBACKS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_CALLBACKS
---

# PRJ_CALLBACKS structure


## -description

A set of callback routines to where the provider stores its implementation of the callback.

## -struct-fields

### -field StartDirectoryEnumerationCallback

A pointer to the StartDirectoryEnumerationCallback.

### -field EndDirectoryEnumerationCallback

A pointer to the EndDirectoryEnumerationCallback.

### -field GetDirectoryEnumerationCallback

A pointer to the GetDirectoryEnumerationCallback.

### -field GetPlaceholderInfoCallback

A pointer to the GetPlaceholderInformationCallback.

### -field GetFileDataCallback

A pointer to the GetFileDataCallback.

### -field QueryFileNameCallback

A pointer to the QueryFileNameCallback.

### -field NotificationCallback

A pointer to the NotifyOperationCallback.

### -field CancelCommandCallback

A pointer to the CancelCommandCallback.


## -remarks

The provider must supply implementations for StartDirectoryEnumerationCallback, EndDirectoryEnumerationCallback, GetDirectoryEnumerationCallback, GetPlaceholderInformationCallback, and GetFileDataCallback. 



The QueryFileNameCallback, NotifyOperationCallback, and CancelCommandCallback callbacks are optional.

<ul>
<li>If the provider does not supply an implementation of QueryFileNameCallback, ProjFS will invoke the directory enumeration callbacks to determine the existence of a file path in the provider's store.</li>
<li>If the provider does not supply an implementation of NotifyOperationCallback, it will not get any notifications from ProjFS.</li>
<li>If the provider does not supply an implementation of CancelCommandCallback, none of the other callbacks will be cancellable. The provider will process all callbacks synchronously.</li>
</ul>

