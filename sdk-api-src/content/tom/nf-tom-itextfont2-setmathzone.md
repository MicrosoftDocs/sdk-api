---
UID: NF:tom.ITextFont2.SetMathZone
title: ITextFont2::SetMathZone
author: windows-sdk-content
description: Sets whether a math zone is active.
old-location: controls\itextfont2_setmathzone.htm
tech.root: controls
ms.assetid: 4e43d51a-3001-4611-8aa1-fcf8cc2655fc
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetMathZone method, ITextFont2.SetMathZone, ITextFont2::SetMathZone, SetMathZone, SetMathZone method [Windows Controls], SetMathZone method [Windows Controls],ITextFont2 interface, controls.itextfont2_setmathzone, tom/ITextFont2::SetMathZone
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITextFont2.SetMathZone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont2::SetMathZone


## -description


Sets whether a math zone is active.


## -parameters




### -param Value [in]

Type: <b>long</b>

A <a href="About_Text_Object_Model.htm">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>A math zone is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>A math zone is not active.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the MathZone property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The MathZone property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/4da4d6d1-16e0-4891-9a60-c1330345e45a">ITextFont2::GetMathZone</a>
 

 

