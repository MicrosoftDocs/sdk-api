---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetHorizontalAlignment
title: IDirectManipulationPrimaryContent::SetHorizontalAlignment method
author: windows-driver-content
description: Sets the horizontal alignment of the primary content relative to the viewport.
old-location: directmanipulation\idirectmanipulationprimarycontent_sethorizontalalignment.htm
old-project: directmanipulation
ms.assetid: 94716ec8-325e-4e9e-9a30-1d9999bdb9c3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDirectManipulationPrimaryContent, IDirectManipulationPrimaryContent interface [Direct Manipulation], SetHorizontalAlignment method, IDirectManipulationPrimaryContent::SetHorizontalAlignment, SetHorizontalAlignment method [Direct Manipulation], SetHorizontalAlignment method [Direct Manipulation], IDirectManipulationPrimaryContent interface, SetHorizontalAlignment,IDirectManipulationPrimaryContent.SetHorizontalAlignment, directmanipulation.idirectmanipulationprimarycontent_sethorizontalalignment, directmanipulation/IDirectManipulationPrimaryContent::SetHorizontalAlignment
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
-	IDirectManipulationPrimaryContent.SetHorizontalAlignment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationPrimaryContent::SetHorizontalAlignment method


## -description


Sets the horizontal alignment of the primary content relative to the viewport.


## -parameters




### -param alignment [in]

One or more values from <a href="https://msdn.microsoft.com/ced17ad6-0728-46ed-8c04-d0c588f0bb38">DIRECTMANIPULATION_HORIZONTALALIGNMENT</a>. The default is <b>DIRECTMANIPULATION_HORIZONTALALIGNMENT_NONE</b>.

<div class="alert"><b>Note</b>  You cannot combine the following options: DIRECTMANIPULATION_HORIZONTALALIGNMENT_LEFT, DIRECTMANIPULATION-HORIZONTALALIGNMENT_CENTER, DIRECTMANIPULATION_HORIZONTALALIGNMENT_RIGHT. DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER can be combined with any option but cannot be configured by itself.</div>
<div> </div>

## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If you have activated a configuration consisting only of zoom or zoom inertia, specify DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER to respect the zoom center point.


#### Examples

The following example shows one way to  this method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT hr = pViewport-&gt;SetHorizontalAlignment(
    DIRECTMANIPULATION_HORIZONTALALIGNMENT_CENTER | DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>
 

 

