---
UID: NF:vss.IVssEnumObject.Clone
title: IVssEnumObject::Clone
author: windows-sdk-content
description: Creates a copy of the specified list of enumerated elements by creating a copy of the IVssEnumObject enumerator object.
old-location: base\ivssenumobject_clone.htm
tech.root: VSS
ms.assetid: 71bf3789-247e-4e3f-8200-a4309a7c2d8c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Clone, Clone method [VSS], Clone method [VSS],IVssEnumObject interface, IVssEnumObject interface [VSS],Clone method, IVssEnumObject.Clone, IVssEnumObject::Clone, _win32_ivssenumobject_clone, base.ivssenumobject_clone, vss/IVssEnumObject::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssEnumObject.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssEnumObject::Clone


## -description


The <b>Clone</b> method creates a copy of the 
    specified list of enumerated elements by creating a copy of the 
    <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> enumerator object.


## -parameters




### -param ppenum

TBD




#### - ppEnum [in, out]

Doubly indirect pointer to an <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> 
      enumerator object. Set the value of this parameter to <b>NULL</b> before calling this 
      method.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There is an internal error in the enumerator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the required pointer parameters is NULL.

</td>
</tr>
</table>
 




## -remarks



The cloned enumerator object will refer to the same list of 
    <a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> structures.

The caller must call the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> method of the 
    returned interface pointer to deallocate the system resources held by the 
    <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> enumerator object pointed to by 
    the <i>ppEnum</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">IVssBackupComponents::Query</a>



<a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a>



<a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a>
 

 

