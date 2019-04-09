---
UID: NF:strmif.IEnumPins.Clone
title: IEnumPins::Clone (strmif.h)
author: windows-sdk-content
description: The Clone method makes a copy of the enumerator with the same enumeration state.
old-location: dshow\ienumpins_clone.htm
tech.root: DirectShow
ms.assetid: 946bb08e-6866-46b3-b2d7-de2ab6c5e608
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [DirectShow], Clone method [DirectShow],IEnumPins interface, IEnumPins interface [DirectShow],Clone method, IEnumPins.Clone, IEnumPins::Clone, IEnumPinsClone, dshow.ienumpins_clone, strmif/IEnumPins::Clone
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
 - IEnumPins.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPins::Clone


## -description



The <code>Clone</code> method makes a copy of the enumerator with the same enumeration state.




## -parameters




### -param ppEnum [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/839190b4-fd29-4a94-8838-d84adfdd9668">IEnumPins</a> interface of the new enumerator. The caller must release the interface.


## -returns



Returns one of the following <b>HRESULT</b>

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
<dt><b>VFW_E_ENUM_OUT_OF_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The filter's state has changed and is now inconsistent with the enumerator.

</td>
</tr>
</table>
 




## -remarks



If the number of pins changes, the enumerator is no longer consistent with the filter, and the method returns VFW_E_ENUM_OUT_OF_SYNC. Discard any data obtained from previous calls to the enumerator, because it might be invalid. Update the enumerator by calling the <a href="https://msdn.microsoft.com/c2147884-aec2-43ae-b85a-61383ad6ca15">IEnumPins::Reset</a> method. You can then call the <code>Clone</code> method safely.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/839190b4-fd29-4a94-8838-d84adfdd9668">IEnumPins Interface</a>
 

 

