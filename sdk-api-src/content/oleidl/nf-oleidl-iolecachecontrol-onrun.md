---
UID: NF:oleidl.IOleCacheControl.OnRun
title: IOleCacheControl::OnRun (oleidl.h)
description: Notifies the cache that the data source object has entered the running state so that the cache object can establish advise sinks as needed.
helpviewer_keywords: ["IOleCacheControl interface [COM]","OnRun method","IOleCacheControl.OnRun","IOleCacheControl::OnRun","OnRun","OnRun method [COM]","OnRun method [COM]","IOleCacheControl interface","_ole_iolecachecontrol_onrun","com.iolecachecontrol_onrun","oleidl/IOleCacheControl::OnRun"]
old-location: com\iolecachecontrol_onrun.htm
tech.root: com
ms.assetid: 8d155c3f-115c-41fe-985f-ed60a565341f
ms.date: 12/05/2018
ms.keywords: IOleCacheControl interface [COM],OnRun method, IOleCacheControl.OnRun, IOleCacheControl::OnRun, OnRun, OnRun method [COM], OnRun method [COM],IOleCacheControl interface, _ole_iolecachecontrol_onrun, com.iolecachecontrol_onrun, oleidl/IOleCacheControl::OnRun
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleCacheControl::OnRun
 - oleidl/IOleCacheControl::OnRun
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleCacheControl.OnRun
---

# IOleCacheControl::OnRun


## -description

Notifies the cache that the data source object has entered the running state so that the cache object can establish advise sinks as needed.

## -parameters

### -param pDataObject [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the object that is entering the running state.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the  arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available for this operation.

</td>
</tr>
</table>

## -remarks

When <b>OnRun</b> is called, the cache sets up advisory connections as necessary with the source data object so it can receive notifications. The advisory connection created between the running object and the cache is destroyed when <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecachecontrol-onstop">IOleCacheControl::OnStop</a> is called.

Some object handlers or in-process servers might use the cache passively, and not call <b>OnRun</b>. These applications must call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache2-updatecache">IOleCache2::UpdateCache</a>, <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-initcache">IOleCache::InitCache</a>, or <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-setdata">IOleCache::SetData</a> to fill the cache when necessary to ensure that the cache gets updated.

<b>OnRun</b> does not add a reference count on the pointer to <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> passed in <i>pDataObject</i>. Because it is the responsibility of the caller of <a href="/windows/desktop/api/ole2/nf-ole2-olerun">OleRun</a> to ensure that the lifetime of the <i>pDataObject</i> pointer lasts until <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecachecontrol-onstop">OnStop</a> is called, the caller must be holding a pointer to <b>IDataObject</b> on the data object of interest.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache2-updatecache">IOleCache2::UpdateCache</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecachecontrol">IOleCacheControl</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecachecontrol-onstop">IOleCacheControl::OnStop</a>