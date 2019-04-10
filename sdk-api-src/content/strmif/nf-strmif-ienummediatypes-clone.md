---
UID: NF:strmif.IEnumMediaTypes.Clone
title: IEnumMediaTypes::Clone (strmif.h)
author: windows-sdk-content
description: The Clone method makes a copy of the enumerator. The returned object starts with the same enumeration state as the original.
old-location: dshow\ienummediatypes_clone.htm
tech.root: DirectShow
ms.assetid: 7a81496d-34e5-43d2-aad9-510ab515adc2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [DirectShow], Clone method [DirectShow],IEnumMediaTypes interface, IEnumMediaTypes interface [DirectShow],Clone method, IEnumMediaTypes.Clone, IEnumMediaTypes::Clone, IEnumMediaTypesClone, dshow.ienummediatypes_clone, strmif/IEnumMediaTypes::Clone
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
 - IEnumMediaTypes.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumMediaTypes::Clone


## -description



The <code>Clone</code> method makes a copy of the enumerator. The returned object starts with the same enumeration state as the original.




## -parameters




### -param ppEnum [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/e0021e27-0e08-4d07-9610-08a9b945ae34">IEnumMediaTypes</a> interface of the new enumerator. The caller must release the interface.


## -returns



Returns one of the following <b>HRESULT</b> values.

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
The pin's state has changed and is now inconsistent with the enumerator.

</td>
</tr>
</table>
 




## -remarks



If the set of media types changes, the enumerator is no longer consistent with the pin, and the method returns VFW_E_ENUM_OUT_OF_SYNC. Discard any data obtained from previous calls to the enumerator, because it might be invalid. Update the enumerator by calling the <a href="https://msdn.microsoft.com/d95d4e69-48dc-4ad1-a0e2-c5fea793b7b3">Reset</a> method. You can then call the <code>Clone</code> method safely.




## -see-also




<a href="https://msdn.microsoft.com/7878885f-c285-4744-8eab-445678dcfd49">Enumerating Media Types</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e0021e27-0e08-4d07-9610-08a9b945ae34">IEnumMediaTypes Interface</a>
 

 

