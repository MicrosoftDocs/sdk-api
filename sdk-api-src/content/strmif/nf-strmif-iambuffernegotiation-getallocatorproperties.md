---
UID: NF:strmif.IAMBufferNegotiation.GetAllocatorProperties
title: IAMBufferNegotiation::GetAllocatorProperties
author: windows-sdk-content
description: The GetAllocatorProperties method retrieves the allocator properties that the pin is using.
old-location: dshow\iambuffernegotiation_getallocatorproperties.htm
old-project: DirectShow
ms.assetid: 85bbb900-772c-4091-83e3-f2a5dd198d39
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetAllocatorProperties, GetAllocatorProperties method [DirectShow], GetAllocatorProperties method [DirectShow],IAMBufferNegotiation interface, IAMBufferNegotiation interface [DirectShow],GetAllocatorProperties method, IAMBufferNegotiation.GetAllocatorProperties, IAMBufferNegotiation::GetAllocatorProperties, IAMBufferNegotiationGetAllocatorProperties, dshow.iambuffernegotiation_getallocatorproperties, strmif/IAMBufferNegotiation::GetAllocatorProperties
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMBufferNegotiation.GetAllocatorProperties
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMBufferNegotiation::GetAllocatorProperties


## -description



The <code>GetAllocatorProperties</code> method retrieves the allocator properties that the pin is using.




## -parameters




### -param pprop [out]

Pointer to an <a href="https://msdn.microsoft.com/813e4693-b549-4045-aff5-08f2dd754b6e">ALLOCATOR_PROPERTIES</a> structure, allocated by the caller, that receives the allocator properties.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/68e98afd-3275-49bb-b165-48ed40026e76">IAMBufferNegotiation Interface</a>
 

 

