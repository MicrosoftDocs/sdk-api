---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUnknown_AtomicRelease function


## -description


Releases a Component Object Model (COM) pointer and sets it to <b>NULL</b>.


## -parameters




### -param ppunk [in, out, optional]

Type: <b>void**</b>

The address of a pointer to a COM interface.


## -returns



This function does not return a value.




## -remarks



If <i>ppunk</i> points to a <b>NULL</b> pointer, no operation is performed. Otherwise, <i>ppunk</i> is assumed to be the address of a COM interface pointer, derived from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. The function calls the interface's <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method then sets the interface pointer to <b>NULL</b>.


#### Examples

The following example uses <b>IUnknown_AtomicRelease</b> to release the stream, if it exists. If not, it does nothing.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void sample()
{
    IStream *pstm = NULL;
    CreateStreamOnHGlobal(NULL, TRUE, &amp;pstm);
    
    IUnknown_AtomicRelease((void**)&amp;pstm);
    
    // At this point, pstm is NULL
}</pre>
</td>
</tr>
</table></span></div>


