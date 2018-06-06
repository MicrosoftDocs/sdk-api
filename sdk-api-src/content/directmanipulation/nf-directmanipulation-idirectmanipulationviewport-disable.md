---
UID: NF:directmanipulation.IDirectManipulationViewport.Disable
title: IDirectManipulationViewport::Disable
author: windows-sdk-content
description: Stops input processing by the viewport.
old-location: directmanipulation\idirectmanipulationviewport_disable.htm
old-project: directmanipulation
ms.assetid: ac4f3cbe-2769-468e-abe3-07b76ada5d7e
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: Disable, Disable method [Direct Manipulation], Disable method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],Disable method, IDirectManipulationViewport.Disable, IDirectManipulationViewport::Disable, directmanipulation.idirectmanipulationviewport_disable, directmanipulation/IDirectManipulationViewport::Disable
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
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.Disable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewport::Disable


## -description


Stops input processing by the viewport.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a viewport is disabled, it immediately stops all transforms and moves the content to the final location. 

Call this method when you want to modify multiple attributes atomically. This method can be called at any time. 

The viewport will not resume processing input until <a href="https://msdn.microsoft.com/library/windows/hardware/hh451004">Enable</a> is called. 


#### Examples

The following example shows how to use this method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT hr = pViewport-&gt;Disable();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

