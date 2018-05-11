---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetVerticalAlignment
title: IDirectManipulationPrimaryContent::SetVerticalAlignment
author: windows-driver-content
description: Specifies the vertical alignment of the primary content in the viewport.
old-location: directmanipulation\idirectmanipulationprimarycontent_setverticalalignment.htm
old-project: directmanipulation
ms.assetid: 111f0358-0955-4ebb-b273-c17d3fb84d75
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetVerticalAlignment method, IDirectManipulationPrimaryContent.SetVerticalAlignment, IDirectManipulationPrimaryContent::SetVerticalAlignment, SetVerticalAlignment, SetVerticalAlignment method [Direct Manipulation], SetVerticalAlignment method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_setverticalalignment, directmanipulation/IDirectManipulationPrimaryContent::SetVerticalAlignment
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
-	IDirectManipulationPrimaryContent.SetVerticalAlignment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationPrimaryContent::SetVerticalAlignment


## -description


Specifies the vertical alignment of the primary content in the viewport.


## -parameters




### -param alignment [in]

One or more values from <a href="https://msdn.microsoft.com/37e9a604-f713-4203-928c-0799206b76fe">DIRECTMANIPULATION_VERTICALALIGNMENT</a>.

<div class="alert"><b>Note</b>  You cannot combine <b>DIRECTMANIPULATION_VERTICALALIGNMENT_TOP</b>, <b>DIRECTMANIPULATION_VERTICALALIGNMENT_CENTER</b>, or <b>DIRECTMANIPULATION_VERTICALALIGNMENT_BOTTOM</b>. <b>DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER</b> can be combined with any option but cannot be configured by itself.</div>
<div> </div>

## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If you have activated a configuration consisting only of zoom or zoom inertia, specify <b>DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER</b> to respect the zoom center point.


#### Examples

The following example shows how to use this method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT hr = pContent-&gt;SetVerticalAlignment(
    DIRECTMANIPULATION_VERTICALALIGNMENT_CENTER| DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>
 

 

