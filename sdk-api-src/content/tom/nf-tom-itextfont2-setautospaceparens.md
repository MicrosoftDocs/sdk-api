---
UID: NF:tom.ITextFont2.SetAutospaceParens
title: ITextFont2::SetAutospaceParens
author: windows-sdk-content
description: Sets the East Asian &#0034;autospace parentheses&#0034; state.
old-location: controls\itextfont2_setautospaceparens.htm
tech.root: Controls
ms.assetid: 9a9290e0-221e-454a-af9c-9d1bf5d37b5e
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetAutospaceParens method, ITextFont2.SetAutospaceParens, ITextFont2::SetAutospaceParens, SetAutospaceParens, SetAutospaceParens method [Windows Controls], SetAutospaceParens method [Windows Controls],ITextFont2 interface, controls.itextfont2_setautospaceparens, tom/ITextFont2::SetAutospaceParens
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
 - ITextFont2.SetAutospaceParens
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont2::SetAutospaceParens


## -description


Sets the East Asian "autospace parentheses" state.


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
<td>Use East Asian autospace parentheses.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not use East Asian autospace parentheses.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the AutospaceParens property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The AutospaceParens property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/fce60349-cded-4cab-b2e5-4fad02d11195">ITextFont2::GetAutospaceParens</a>
 

 

