---
UID: NF:strmif.IAMBufferNegotiation.GetAllocatorProperties
title: IAMBufferNegotiation::GetAllocatorProperties (strmif.h)
description: The GetAllocatorProperties method retrieves the allocator properties that the pin is using.helpviewer_keywords: ["GetAllocatorProperties","GetAllocatorProperties method [DirectShow]","GetAllocatorProperties method [DirectShow]","IAMBufferNegotiation interface","IAMBufferNegotiation interface [DirectShow]","GetAllocatorProperties method","IAMBufferNegotiation.GetAllocatorProperties","IAMBufferNegotiation::GetAllocatorProperties","IAMBufferNegotiationGetAllocatorProperties","dshow.iambuffernegotiation_getallocatorproperties","strmif/IAMBufferNegotiation::GetAllocatorProperties"]
old-location: dshow\iambuffernegotiation_getallocatorproperties.htm
tech.root: DirectShow
ms.assetid: 85bbb900-772c-4091-83e3-f2a5dd198d39
ms.date: 12/05/2018
ms.keywords: GetAllocatorProperties, GetAllocatorProperties method [DirectShow], GetAllocatorProperties method [DirectShow],IAMBufferNegotiation interface, IAMBufferNegotiation interface [DirectShow],GetAllocatorProperties method, IAMBufferNegotiation.GetAllocatorProperties, IAMBufferNegotiation::GetAllocatorProperties, IAMBufferNegotiationGetAllocatorProperties, dshow.iambuffernegotiation_getallocatorproperties, strmif/IAMBufferNegotiation::GetAllocatorProperties
f1_keywords:
- strmif/IAMBufferNegotiation.GetAllocatorProperties
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
- IAMBufferNegotiation.GetAllocatorProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMBufferNegotiation::GetAllocatorProperties


## -description



The <code>GetAllocatorProperties</code> method retrieves the allocator properties that the pin is using.




## -parameters




### -param pprop [out]

Pointer to an [ALLOCATOR_PROPERTIES](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-allocator_properties) structure, allocated by the caller, that receives the allocator properties.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Pin is not connected.

</td>
</tr>
</table>
 




## -remarks



Call this method after the pins connect, to find out the allocator properties that were chosen.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iambuffernegotiation">IAMBufferNegotiation Interface</a>
 

 

