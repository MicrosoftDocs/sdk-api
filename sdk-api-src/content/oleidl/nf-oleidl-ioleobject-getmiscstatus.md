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

# IOleObject::GetMiscStatus


## -description


Retrieves the status of an object at creation and loading.


## -parameters




### -param dwAspect [in]

The aspect of an object about which status information is being requested. The value is obtained from the enumeration <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a>.


### -param pdwStatus [out]

Pointer to where the status information is returned. This parameter cannot be <b>NULL</b>.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_S_USEREG</b></dt>
</dl>
</td>
<td width="60%">
Delegate the retrieval of miscellaneous status information to the default handler's implementation of this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
There is no CLSID registered for the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_READREGDB</b></dt>
</dl>
</td>
<td width="60%">
Error accessing the registry.

</td>
</tr>
</table>
 




## -remarks



A container normally calls <b>IOleObject::GetMiscStatus</b> when it creates or loads an object in order to determine how to display the object and what types of behaviors it supports.

Objects store status information in the registry. If the object is not running, the default handler's implementation of <b>IOleObject::GetMiscStatus</b> retrieves this information from the registry. If the object is running, the default handler invokes <b>IOleObject::GetMiscStatus</b> on the object itself.

The information that is actually stored in the registry varies with individual objects. The status values to be returned are defined in the enumeration <a href="https://msdn.microsoft.com/0a90d126-fc28-460c-8eaf-cf98ae998f95">OLEMISC</a>.

The default value of <b>IOleObject::GetMiscStatus</b> is used if a subkey corresponding to the specified <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a> is not found. To set an OLE control, specify DVASPECT==1. This will cause the following to occur in the registry: 


<pre xml:space="preserve"><b>HKEY_CLASSES_ROOT\CLSID\ . . .</b>
   <b>MiscStatus</b> = 1</pre>


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Implementation normally consists of delegating the call to the default handler.




## -see-also




<a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a>



<a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/0a90d126-fc28-460c-8eaf-cf98ae998f95">OLEMISC</a>
 

 

