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

# IUnknown_Set function


## -description


Changes the value of a Component Object Model (COM) interface pointer and releases the previous interface.


## -parameters




### -param ppunk [in, out]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

The address of a COM interface pointer to receive the pointer assigned to <i>punk</i>. If the previous value of the pointer is non-<b>NULL</b>, the function releases that interface by calling its IUnkown::Release method.


### -param punk [in, optional]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

The interface pointer to be copied to <i>ppunk</i>. If the value is non-<b>NULL</b>, the function increments the interface's reference count.


## -returns



This function does not return a value.




## -remarks



This function mimics the behavior of a smart pointer. Conceptually, the function does the following:
                
                

<ul>
<li>Releases the original interface, if <i>ppunk</i> is non-<b>NULL</b></li>
<li>Assigns <i>punk</i> to <i>ppunk</i></li>
<li>Calls IUnknown::AddRef on the interface pointed to by <i>punk</i>, if <i>punk</i> is non-<b>NULL</b>.</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
void sample()
{
  IUnknown *punk = NULL;
  IStream* pstm = NULL;

  if (SUCCEEDED(CreateStreamOnHGlobal(NULL, TRUE, &amp;pstm)) {
    // since punk == NULL, this merely copies the value and AddRef()s it
    IUnknown_Set(&amp;punk, pstm);
    pstm-&gt;Release();

    if (SUCCEEDED(CreateStreamOnHGlobal(NULL, TRUE, &amp;pstm)) {
      // this call will release the old value of punk before copying the
      // new value and AddRef()ing it
      IUnknown_Set(&amp;punk, pstm);
      pstm-&gt;Release();
    }
  }

  // This call will release whatever punk points to, if anything.
  IUnknown_AtomcRelease((void**)&amp;punk);

  // at this point, punk == NULL
}</pre>
</td>
</tr>
</table></span></div>


