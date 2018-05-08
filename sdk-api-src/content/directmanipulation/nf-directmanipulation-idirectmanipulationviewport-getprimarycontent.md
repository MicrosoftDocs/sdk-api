---
UID: NF:directmanipulation.IDirectManipulationViewport.GetPrimaryContent
title: IDirectManipulationViewport::GetPrimaryContent
author: windows-driver-content
description: Gets the primary content of a viewport that implements IDirectManipulationContent and IDirectManipulationPrimaryContent.
old-location: directmanipulation\idirectmanipulationviewport_getprimarycontent.htm
old-project: directmanipulation
ms.assetid: 1aa70be3-9e95-4c35-8cca-45c1b238961e
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetPrimaryContent, GetPrimaryContent method [Direct Manipulation], GetPrimaryContent method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],GetPrimaryContent method, IDirectManipulationViewport.GetPrimaryContent, IDirectManipulationViewport::GetPrimaryContent, directmanipulation.idirectmanipulationviewport_getprimarycontent, directmanipulation/IDirectManipulationViewport::GetPrimaryContent
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IDirectManipulationViewport.GetPrimaryContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewport::GetPrimaryContent


## -description


Gets the primary content of a viewport that implements <a href="https://msdn.microsoft.com/4d69a503-f998-4197-824f-4df48825c941">IDirectManipulationContent</a> and <a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>. 

Primary content is an element that gets transformed (e.g. moved, scaled, rotated) in response to a user interaction. Primary content is created at the same time as the viewport and cannot be added or removed.


## -parameters




### -param riid [in]

IID to the interface.


### -param object [out, retval]

The primary content object.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



    This method gets the content of the viewport that implements <a href="https://msdn.microsoft.com/4d69a503-f998-4197-824f-4df48825c941">IDirectManipulationContent</a> and <a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>.



#### Examples

The following example shows how to use this method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IDirectManipulationPrimaryContent *pContent;

HRESULT hr = pRegion-&gt;GetPrimaryContent(IID_PPV_ARGS(&amp;pContent));
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

