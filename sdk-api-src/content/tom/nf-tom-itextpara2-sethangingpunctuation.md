---
UID: NF:tom.ITextPara2.SetHangingPunctuation
title: ITextPara2::SetHangingPunctuation
author: windows-sdk-content
description: Sets whether to hang punctuation symbols on the right margin when the paragraph is justified.
old-location: controls\itextpara2_sethangingpunctuation.htm
old-project: Controls
ms.assetid: 8c70f76f-7a4a-49b3-bc16-8e90ad7ee041
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetHangingPunctuation method, ITextPara2.SetHangingPunctuation, ITextPara2::SetHangingPunctuation, SetHangingPunctuation, SetHangingPunctuation method [Windows Controls], SetHangingPunctuation method [Windows Controls],ITextPara2 interface, controls.itextpara2_sethangingpunctuation, tom/ITextPara2::SetHangingPunctuation
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
 - ITextPara2.SetHangingPunctuation
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara2::SetHangingPunctuation


## -description


Sets whether to hang
 punctuation symbols on the right margin when the paragraph is justified.


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
<td>Hang
 punctuation symbols on the right margin.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not hang
 punctuation symbols on the right margin.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the HangingPunctuation property.</td>
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



<a href="https://msdn.microsoft.com/781b7c53-e9a1-4c4a-84d7-ea70efc173d1">ITextPara2::GetHangingPunctuation</a>
 

 

