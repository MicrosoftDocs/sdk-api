---
UID: NF:directmanipulation.IDirectManipulationViewport.Enable
title: IDirectManipulationViewport::Enable
author: windows-sdk-content
description: Starts or resumes input processing by the viewport.
old-location: directmanipulation\idirectmanipulationviewport_enable.htm
tech.root: directmanipulation
ms.assetid: 47ebb502-26c6-4bff-8baf-bd825fc06755
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Enable, Enable method [Direct Manipulation], Enable method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],Enable method, IDirectManipulationViewport.Enable, IDirectManipulationViewport::Enable, directmanipulation.idirectmanipulationviewport_enable, directmanipulation/IDirectManipulationViewport::Enable
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.Enable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationViewport::Enable


## -description


Starts or resumes input processing by the viewport.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>, or <b>S_FALSE</b> if there is no work to do (for example, the viewport is already enabled). Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method directs a viewport to attempt to respond to input.

Call this method if the <b>AUTODISABLE</b> option is set. 


#### Examples

The following example shows how to use this method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT hr = pViewport-&gt;Enable();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

