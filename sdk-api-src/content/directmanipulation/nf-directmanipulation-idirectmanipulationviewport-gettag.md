---
UID: NF:directmanipulation.IDirectManipulationViewport.GetTag
title: IDirectManipulationViewport::GetTag
author: windows-sdk-content
description: Gets the tag value of a viewport.
old-location: directmanipulation\idirectmanipulationviewport_gettag.htm
old-project: directmanipulation
ms.assetid: 7523a99b-de43-4efe-ae22-6632167c039a
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetTag, GetTag method [Direct Manipulation], GetTag method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],GetTag method, IDirectManipulationViewport.GetTag, IDirectManipulationViewport::GetTag, directmanipulation.idirectmanipulationviewport_gettag, directmanipulation/IDirectManipulationViewport::GetTag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectManipulation.h
api_name:
-	IDirectManipulationViewport.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

