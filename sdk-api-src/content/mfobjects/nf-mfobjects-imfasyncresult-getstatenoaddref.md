---
UID: NF:mfobjects.IMFAsyncResult.GetStateNoAddRef
title: IMFAsyncResult::GetStateNoAddRef (mfobjects.h)
description: Returns the state object specified by the caller in the asynchronous Begin method, without incrementing the object's reference count. (IMFAsyncResult.GetStateNoAddRef)
helpviewer_keywords: ["37ba820c-5253-48de-a960-c546e50e8672","GetStateNoAddRef","GetStateNoAddRef method [Media Foundation]","GetStateNoAddRef method [Media Foundation]","IMFAsyncResult interface","IMFAsyncResult interface [Media Foundation]","GetStateNoAddRef method","IMFAsyncResult.GetStateNoAddRef","IMFAsyncResult::GetStateNoAddRef","mf.imfasyncresult_getstatenoaddref","mfobjects/IMFAsyncResult::GetStateNoAddRef"]
old-location: mf\imfasyncresult_getstatenoaddref.htm
tech.root: mf
ms.assetid: 37ba820c-5253-48de-a960-c546e50e8672
ms.date: 12/05/2018
ms.keywords: 37ba820c-5253-48de-a960-c546e50e8672, GetStateNoAddRef, GetStateNoAddRef method [Media Foundation], GetStateNoAddRef method [Media Foundation],IMFAsyncResult interface, IMFAsyncResult interface [Media Foundation],GetStateNoAddRef method, IMFAsyncResult.GetStateNoAddRef, IMFAsyncResult::GetStateNoAddRef, mf.imfasyncresult_getstatenoaddref, mfobjects/IMFAsyncResult::GetStateNoAddRef
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAsyncResult::GetStateNoAddRef
 - mfobjects/IMFAsyncResult::GetStateNoAddRef
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAsyncResult.GetStateNoAddRef
---

# IMFAsyncResult::GetStateNoAddRef


## -description

Returns the state object specified by the caller in the asynchronous <b>Begin</b> method, without incrementing the object's reference count.



## -returns

Returns a pointer to the state object's <b>IUnknown</b> interface, or <b>NULL</b> if no object was set. This pointer does not have an outstanding reference count. If you store this pointer, you must call <b>AddRef</b> on the pointer.

## -remarks

This method cannot be called remotely.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a>
