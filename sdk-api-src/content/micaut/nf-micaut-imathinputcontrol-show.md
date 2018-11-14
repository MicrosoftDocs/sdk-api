---
UID: NF:micaut.IMathInputControl.Show
title: IMathInputControl::Show
author: windows-sdk-content
description: Shows the control.
old-location: tablet\imathinputcontrol_show.htm
tech.root: tablet
ms.assetid: d45d1e73-eace-4611-a4a4-28706a19766c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMathInputControl interface [Tablet PC],Show method, IMathInputControl.Show, IMathInputControl::Show, Show, Show method [Tablet PC], Show method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::Show, tablet.imathinputcontrol_show
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: micaut.h
req.include-header: Micaut.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Micaut.idl
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
 - micaut.h
api_name:
 - IMathInputControl.Show
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- micaut.h
: 
- IMathInputControl.Show
: 
---

# IMathInputControl::Show


## -description


Shows the control.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Shows the Math Input Control if it is not visible. If the control is already visible, puts the control on top of the z-order stack.
If <a href="https://msdn.microsoft.com/9b5fc988-7c93-47d4-8661-4cef56cab0d0">SetPosition</a> is not called, <b>Show</b> will display the control at the top-left corner of the screen ((0, 0) in screen cooridnates). 
The control's width and height will be at their minimum.
	 


#### Examples

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
    HRESULT hr = CoInitialize(NULL);
    hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
    hr = g_spMIC-&gt;EnableExtendedButtons(VARIANT_TRUE);
    hr = g_spMIC-&gt;Show();  
    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/59976b01-9032-4226-a160-e9b2d4b8b23b">Creating a Math Input Control</a>



<a href="https://msdn.microsoft.com/922562be-4d5b-45b6-ad0b-49176f893c8e">Customizing the Math Input Control</a>



<a href="https://msdn.microsoft.com/13b227bf-3ea5-4da1-998e-8809616d88b6">Hide</a>



<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>
 

 

