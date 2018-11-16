---
UID: NF:tom.ITextPara2.GetHangingPunctuation
title: ITextPara2::GetHangingPunctuation
author: windows-sdk-content
description: Gets whether to hang punctuation symbols on the right margin when the paragraph is justified.
old-location: controls\itextpara2_gethangingpunctuation.htm
tech.root: Controls
ms.assetid: 781b7c53-e9a1-4c4a-84d7-ea70efc173d1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetHangingPunctuation, GetHangingPunctuation method [Windows Controls], GetHangingPunctuation method [Windows Controls],ITextPara2 interface, ITextPara2 interface [Windows Controls],GetHangingPunctuation method, ITextPara2.GetHangingPunctuation, ITextPara2::GetHangingPunctuation, controls.itextpara2_gethangingpunctuation, tom/ITextPara2::GetHangingPunctuation
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
 - ITextPara2.GetHangingPunctuation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tom.h
: 
- ITextPara2.GetHangingPunctuation
: 
---

# ITextPara2::GetHangingPunctuation


## -description


Gets whether to hang
 punctuation symbols on the right margin when the paragraph is justified.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb787724(v=VS.85).aspx">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Hang
 punctuation symbols on the right margin.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not hang
 punctuation symbols on the right margin.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The HangingPunctuation property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>



<a href="https://msdn.microsoft.com/8c70f76f-7a4a-49b3-bc16-8e90ad7ee041">ITextPara2::SetHangingPunctuation</a>
 

 

