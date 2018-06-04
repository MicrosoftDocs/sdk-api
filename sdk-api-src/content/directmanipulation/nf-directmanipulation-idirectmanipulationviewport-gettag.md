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

# IDirectManipulationViewport::GetTag


## -description


Gets the tag value of a viewport.


## -parameters




### -param riid [in]

IID to the interface.


### -param object [out, optional]

The object portion of the tag.


### -param id [out, optional]

The identifier portion of the tag.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



A tag is a pairing of an integer ID with a Component Object Model (COM) object. It can be used by an app to identify the viewport.


The out parameters are optional, so the method can return an ID, the viewport object, or both.



#### Examples

The following example show how to use this method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IUnknown* pUnk;
UINT32 id;

HRESULT hr = pRegion-&gt;GetTag(IID_PPV_ARGS(&amp;pUnk), &amp;id); 

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

