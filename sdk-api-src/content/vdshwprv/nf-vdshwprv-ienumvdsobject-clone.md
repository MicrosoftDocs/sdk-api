---
UID: NF:vdshwprv.IEnumVdsObject.Clone
title: IEnumVdsObject::Clone (vdshwprv.h)
author: windows-sdk-content
description: Creates an enumeration with the same state as the current enumeration.
old-location: base\ienumvdsobject_clone.htm
tech.root: VDS
ms.assetid: 9d547011-2200-43fc-a8de-9b90ba94c39e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [VDS], Clone method [VDS],IEnumVdsObject interface, IEnumVdsObject interface [VDS],Clone method, IEnumVdsObject.Clone, IEnumVdsObject::Clone, base.ienumvdsobject_clone, vds/IEnumVdsObject::Clone, vdshwprv/IEnumVdsObject::Clone
ms.topic: method
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IEnumVdsObject.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumVdsObject::Clone


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Creates an enumeration 
   with the same state as the current enumeration.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> pointer, which 
      VDS initializes on return. Callers must release the interface.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The new enumeration has been created.

</td>
</tr>
</table>
 




## -remarks



This method enables you to record a point in an enumeration and return to that point later. When the new, 
    cloned enumeration is returned, it is at the same point in the enumeration sequence as the original. Henceforth, 
    however, the clone and the original enumeration operate independently.




## -see-also




<a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a>
 

 

