---
UID: NF:tom.ITextFont2.GetMathZone
title: ITextFont2::GetMathZone
author: windows-sdk-content
description: Gets whether a math zone is active.
old-location: controls\itextfont2_getmathzone.htm
tech.root: controls
ms.assetid: 4da4d6d1-16e0-4891-9a60-c1330345e45a
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetMathZone, GetMathZone method [Windows Controls], GetMathZone method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetMathZone method, ITextFont2.GetMathZone, ITextFont2::GetMathZone, controls.itextfont2_getmathzone, tom/ITextFont2::GetMathZone
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
 - ITextFont2.GetMathZone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont2::GetMathZone


## -description


Gets whether a math zone is active.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

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
<td><b>tomUndefined</b></td>
<td>The MathZone property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/4e43d51a-3001-4611-8aa1-fcf8cc2655fc">ITextFont2::SetMathZone</a>
 

 

