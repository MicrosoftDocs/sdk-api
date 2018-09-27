---
UID: NF:strmif.IMemInputPin.GetAllocatorRequirements
title: IMemInputPin::GetAllocatorRequirements
author: windows-sdk-content
description: The GetAllocatorRequirements method retrieves the allocator properties requested by the input pin.
old-location: dshow\imeminputpin_getallocatorrequirements.htm
tech.root: DirectShow
ms.assetid: 61e6ea4f-70cd-43d8-bbb7-76e041ee0eeb
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetAllocatorRequirements, GetAllocatorRequirements method [DirectShow], GetAllocatorRequirements method [DirectShow],IMemInputPin interface, IMemInputPin interface [DirectShow],GetAllocatorRequirements method, IMemInputPin.GetAllocatorRequirements, IMemInputPin::GetAllocatorRequirements, IMemInputPinGetAllocatorRequirements, dshow.imeminputpin_getallocatorrequirements, strmif/IMemInputPin::GetAllocatorRequirements
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
 - IMemInputPin.GetAllocatorRequirements
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMemInputPin::GetAllocatorRequirements


## -description



The <code>GetAllocatorRequirements</code> method retrieves the allocator properties requested by the input pin.




## -parameters




### -param pProps [in]

Pointer to an <a href="https://msdn.microsoft.com/813e4693-b549-4045-aff5-08f2dd754b6e">ALLOCATOR_PROPERTIES</a>, structure which is filled in with the requirements.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented

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



When an output pin initializes a memory allocator, it can call this method to determine whether the input pin has any buffer requirements. The input pin is not required to implement this method. If the filter has specific alignment or prefix requirements, it should implement this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin Interface</a>
 

 

