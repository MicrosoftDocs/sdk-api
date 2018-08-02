---
UID: NF:tom.ITextFont2.GetAutoLigatures
title: ITextFont2::GetAutoLigatures
author: windows-sdk-content
description: Gets whether support for automatic ligatures is active.
old-location: controls\itextfont2_getautoligatures.htm
old-project: Controls
ms.assetid: f8209c34-139c-45e6-b110-f6d3d76f5575
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetAutoLigatures, GetAutoLigatures method [Windows Controls], GetAutoLigatures method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetAutoLigatures method, ITextFont2.GetAutoLigatures, ITextFont2::GetAutoLigatures, controls.itextfont2_getautoligatures, tom/ITextFont2::GetAutoLigatures
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
 - ITextFont2.GetAutoLigatures
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetAutoLigatures


## -description


Gets whether support for automatic ligatures is active.


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
<td>Automatic ligature support is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Automatic ligature support is not active.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The AutoLigatures property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/f40fecfe-3c3b-46f0-9edf-ba48236e50e7">ITextFont2::SetAutoLigatures</a>
 

 

