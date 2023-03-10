---
UID: NF:mfobjects.IMFAttributes.LockStore
title: IMFAttributes::LockStore (mfobjects.h)
description: Locks the attribute store so that no other thread can access it.
helpviewer_keywords: ["6ec7aed3-7dbc-4aa4-92d5-646aee757db7","IMFAttributes interface [Media Foundation]","LockStore method","IMFAttributes.LockStore","IMFAttributes::LockStore","LockStore","LockStore method [Media Foundation]","LockStore method [Media Foundation]","IMFAttributes interface","mf.imfattributes_lockstore","mfobjects/IMFAttributes::LockStore"]
old-location: mf\imfattributes_lockstore.htm
tech.root: mf
ms.assetid: 6ec7aed3-7dbc-4aa4-92d5-646aee757db7
ms.date: 12/05/2018
ms.keywords: 6ec7aed3-7dbc-4aa4-92d5-646aee757db7, IMFAttributes interface [Media Foundation],LockStore method, IMFAttributes.LockStore, IMFAttributes::LockStore, LockStore, LockStore method [Media Foundation], LockStore method [Media Foundation],IMFAttributes interface, mf.imfattributes_lockstore, mfobjects/IMFAttributes::LockStore
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
 - IMFAttributes::LockStore
 - mfobjects/IMFAttributes::LockStore
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
 - IMFAttributes.LockStore
---

# IMFAttributes::LockStore


## -description

Locks the attribute store so that no other thread can access it. If the attribute store is already locked by another thread, this method blocks until the other thread unlocks the object. After calling this method, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-unlockstore">IMFAttributes::UnlockStore</a> to unlock the object.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method can cause a deadlock if a thread that calls <b>LockStore</b> waits on a thread that calls any other <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> methods on the same object.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>
