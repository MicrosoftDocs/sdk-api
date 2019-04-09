---
UID: NF:tom.ITextFont2.SetOverlapping
title: ITextFont2::SetOverlapping (tom.h)
author: windows-sdk-content
description: Sets whether overlapping text is active.
old-location: controls\itextfont2_setoverlapping.htm
tech.root: Controls
ms.assetid: 40addd31-5c0e-45bd-a649-c65973ae8340
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetOverlapping method, ITextFont2.SetOverlapping, ITextFont2::SetOverlapping, SetOverlapping, SetOverlapping method [Windows Controls], SetOverlapping method [Windows Controls],ITextFont2 interface, controls.itextfont2_setoverlapping, tom/ITextFont2::SetOverlapping
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont2.SetOverlapping
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont2::SetOverlapping


## -description


Sets whether overlapping text is active.


## -parameters




### -param Value [in]

Type: <b>long</b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb787724(v=VS.85).aspx">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Overlapping text is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Overlapping text is not active.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the Overlapping property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Overlapping property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/26937777-a44b-4196-aa6b-f35787f934a9">ITextFont2::GetOverlapping</a>
 

 

