---
UID: NF:strmif.IPin.EnumMediaTypes
title: IPin::EnumMediaTypes
author: windows-sdk-content
description: The EnumMediaTypes method enumerates the pin's preferred media types.
old-location: dshow\ipin_enummediatypes.htm
old-project: DirectShow
ms.assetid: 288be4db-5236-40e5-bd92-d95b1bfb86fa
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: EnumMediaTypes, EnumMediaTypes method [DirectShow], EnumMediaTypes method [DirectShow],IPin interface, IPin interface [DirectShow],EnumMediaTypes method, IPin.EnumMediaTypes, IPin::EnumMediaTypes, IPinEnumMediaTypes, dshow.ipin_enummediatypes, strmif/IPin::EnumMediaTypes
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IPin.EnumMediaTypes
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IPin::EnumMediaTypes


## -description



The <b>EnumMediaTypes</b> method enumerates the pin's preferred media types.




## -parameters




### -param ppEnum [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/e0021e27-0e08-4d07-9610-08a9b945ae34">IEnumMediaTypes</a> interface. The caller must release the interface.
          


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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected. Some pins do not enumerate media types unless the pin is connected to another filter.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/e0021e27-0e08-4d07-9610-08a9b945ae34">IEnumMediaTypes</a> interface works like a standard COM enumerator. For more information, see <a href="https://msdn.microsoft.com/04a3dbc8-33c4-4b70-930e-686be2f8301f">Enumerating Objects in a Filter Graph</a>. If the method succeeds, the <b>IEnumMediaTypes</b> interface has an outstanding reference count. Be sure to release it when you are done.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 

