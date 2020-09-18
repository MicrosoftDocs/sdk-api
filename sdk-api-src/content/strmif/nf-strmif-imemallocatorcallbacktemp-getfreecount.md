---
UID: NF:strmif.IMemAllocatorCallbackTemp.GetFreeCount
title: IMemAllocatorCallbackTemp::GetFreeCount (strmif.h)
description: The GetFreeCount method returns the number of free media samples. This number equals the total number of media samples minus the number of samples that are currently held by filters.
helpviewer_keywords: ["GetFreeCount","GetFreeCount method [DirectShow]","GetFreeCount method [DirectShow]","IMemAllocatorCallbackTemp interface","IMemAllocatorCallbackTemp interface [DirectShow]","GetFreeCount method","IMemAllocatorCallbackTemp.GetFreeCount","IMemAllocatorCallbackTemp::GetFreeCount","IMemAllocatorCallbackTempGetFreeCount","dshow.imemallocatorcallbacktemp_getfreecount","strmif/IMemAllocatorCallbackTemp::GetFreeCount"]
old-location: dshow\imemallocatorcallbacktemp_getfreecount.htm
tech.root: dshow
ms.assetid: 2dd0cdb3-664a-4022-b8bb-fda759172dd6
ms.date: 12/05/2018
ms.keywords: GetFreeCount, GetFreeCount method [DirectShow], GetFreeCount method [DirectShow],IMemAllocatorCallbackTemp interface, IMemAllocatorCallbackTemp interface [DirectShow],GetFreeCount method, IMemAllocatorCallbackTemp.GetFreeCount, IMemAllocatorCallbackTemp::GetFreeCount, IMemAllocatorCallbackTempGetFreeCount, dshow.imemallocatorcallbacktemp_getfreecount, strmif/IMemAllocatorCallbackTemp::GetFreeCount
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMemAllocatorCallbackTemp::GetFreeCount
 - strmif/IMemAllocatorCallbackTemp::GetFreeCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMemAllocatorCallbackTemp.GetFreeCount
---

# IMemAllocatorCallbackTemp::GetFreeCount


## -description

The <code>GetFreeCount</code> method returns the number of free media samples. This number equals the total number of media samples minus the number of samples that are currently held by filters.

## -parameters

### -param plBuffersFree [out]

Pointer to a variable that receives the number of free media samples.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

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

A filter holds a sample by keeping a reference count on it. It releases the sample by releasing the reference count.

Until the allocator is committed, the samples are not guaranteed to be allocated.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imemallocatorcallbacktemp">IMemAllocatorCallbackTemp Interface</a>