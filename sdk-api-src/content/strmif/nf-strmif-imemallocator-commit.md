---
UID: NF:strmif.IMemAllocator.Commit
title: IMemAllocator::Commit (strmif.h)
description: The Commit method allocates the buffer memory.
helpviewer_keywords: ["Commit","Commit method [DirectShow]","Commit method [DirectShow]","IMemAllocator interface","IMemAllocator interface [DirectShow]","Commit method","IMemAllocator.Commit","IMemAllocator::Commit","IMemAllocatorCommit","dshow.imemallocator_commit","strmif/IMemAllocator::Commit"]
old-location: dshow\imemallocator_commit.htm
tech.root: dshow
ms.assetid: 34db4c1f-5642-4495-a572-9a78b1ee7b7e
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [DirectShow], Commit method [DirectShow],IMemAllocator interface, IMemAllocator interface [DirectShow],Commit method, IMemAllocator.Commit, IMemAllocator::Commit, IMemAllocatorCommit, dshow.imemallocator_commit, strmif/IMemAllocator::Commit
f1_keywords:
- strmif/IMemAllocator.Commit
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMemAllocator.Commit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMemAllocator::Commit


## -description



The <code>Commit</code> method allocates the buffer memory.




## -parameters






## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_SIZENOTSET</b></dt>
</dl>
</td>
<td width="60%">
Buffer requirements were not set.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-setproperties">IMemAllocator::SetProperties</a> method to specify the buffer requirements.

You must call this method before calling the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-getbuffer">IMemAllocator::GetBuffer</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator Interface</a>
 

 

