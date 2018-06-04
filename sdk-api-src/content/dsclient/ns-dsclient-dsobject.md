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

# DSOBJECT structure


## -description


The <b>DSOBJECT</b> structure contains directory object data. An array of this structure is provided in the <b>aObjects</b> member of the <a href="https://msdn.microsoft.com/dfc1e88f-40ff-4ec1-9718-4801f678fa3f">DSOBJECTNAMES</a> structure.


## -struct-fields




### -field dwFlags

Contains a set of flags that provide object data. This can be zero or a combination of one, or more, of the following values.



#### DSOBJECT_ISCONTAINER

The object is a container.



#### DSOBJECT_READONLYPAGES

When displaying properties for this object, the user interface must be read-only.


### -field dwProviderFlags

Contains a set of flags that provide data about the object provider. This can be zero or a combination of one or more of the following values.



#### DSPROVIDER_ADVANCED

The user interface for this object should be shown in an advanced mode.



#### DSPROVIDER_UNUSED_0

Not used.



#### DSPROVIDER_UNUSED_1

Not used.



#### DSPROVIDER_UNUSED_2

Not used.



#### DSPROVIDER_UNUSED_3

Not used.


### -field offsetName

Contains the offset, in bytes, from the start of the <a href="https://msdn.microsoft.com/dfc1e88f-40ff-4ec1-9718-4801f678fa3f">DSOBJECTNAMES</a> structure to a NULL-terminated, Unicode string that contains the ADSPath of the object.

The following code example shows how to use this member.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>pwszName = (LPWSTR)((LPBYTE)pdsObjNames + 
    pdsObjNames-&gt;aObjects[i].offsetName);
</pre>
</td>
</tr>
</table></span></div>

### -field offsetClass

Contains the offset, in bytes, from the start of the <a href="https://msdn.microsoft.com/dfc1e88f-40ff-4ec1-9718-4801f678fa3f">DSOBJECTNAMES</a> structure to a NULL-terminated, Unicode string that contains the class name of the object. Contains zero if the class name is unknown.

The following code example shows how to use this member.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>pwszClass = (LPWSTR)((LPBYTE)pdsObjNames + 
    pdsObjNames-&gt;aObjects[i].offsetClass);
</pre>
</td>
</tr>
</table></span></div>

## -see-also




<a href="https://msdn.microsoft.com/dfc1e88f-40ff-4ec1-9718-4801f678fa3f">DSOBJECTNAMES</a>



<a href="https://msdn.microsoft.com/bf6aa066-ee7e-4b13-9a4b-1e097632ec5a">Display Structures in Active Directory Domain Services</a>
 

 

