---
UID: NF:strmif.IMediaFilter.GetSyncSource
title: IMediaFilter::GetSyncSource
author: windows-sdk-content
description: The GetSyncSource method retrieves the current reference clock.
old-location: dshow\imediafilter_getsyncsource.htm
tech.root: DirectShow
ms.assetid: 5f5eb31c-3a12-45f4-9c95-caafc0267481
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetSyncSource, GetSyncSource method [DirectShow], GetSyncSource method [DirectShow],IMediaFilter interface, IMediaFilter interface [DirectShow],GetSyncSource method, IMediaFilter.GetSyncSource, IMediaFilter::GetSyncSource, IMediaFilterGetSyncSource, dshow.imediafilter_getsyncsource, strmif/IMediaFilter::GetSyncSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMediaFilter.GetSyncSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IMediaFilter.GetSyncSource
: 
---

# IMediaFilter::GetSyncSource


## -description



The <code>GetSyncSource</code> method retrieves the current reference clock.




## -parameters




### -param pClock [out]

Receives a pointer to the clock's <a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock</a> interface. The caller must release the interface.


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
Success

</td>
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
</table>
 




## -remarks



This method returns the same reference clock as the last call to <a href="https://msdn.microsoft.com/a374c963-cc28-41f6-814d-7ffc6efc67a6">IMediaFilter::SetSyncSource</a>. If there is no reference clock, <i>pClock</i> receives the value <b>NULL</b>. When the method returns, if <i>*pClock</i> is non-<b>NULL</b>, the <b>IReferenceClock</b> interface has an outstanding reference count. Be sure to release it when you are done.

You can also call this method on the Filter Graph Manager to determine the current reference clock.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5c0060e8-a9e5-4141-a38d-9a1bc55cc91b">IMediaFilter Interface</a>
 

 

