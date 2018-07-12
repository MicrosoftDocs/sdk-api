---
UID: NF:tom.ITextFont2.GetOverlapping
title: ITextFont2::GetOverlapping
author: windows-sdk-content
description: Gets whether overlapping text is active.
old-location: controls\itextfont2_getoverlapping.htm
old-project: controls
ms.assetid: 26937777-a44b-4196-aa6b-f35787f934a9
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: GetOverlapping, GetOverlapping method [Windows Controls], GetOverlapping method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetOverlapping method, ITextFont2.GetOverlapping, ITextFont2::GetOverlapping, controls.itextfont2_getoverlapping, tom/ITextFont2::GetOverlapping
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont2.GetOverlapping
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetOverlapping


## -description


Gets whether overlapping text is active.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="https://msdn.microsoft.com/library/Bb787724(v=VS.85).aspx">tomBool</a> value that can be one of the following.

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
<td><b>tomUndefined</b></td>
<td>The Overlapping property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/40addd31-5c0e-45bd-a649-c65973ae8340">ITextFont2::SetOverlapping</a>
 

 

