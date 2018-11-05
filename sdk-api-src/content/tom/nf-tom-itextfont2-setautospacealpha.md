---
UID: NF:tom.ITextFont2.SetAutospaceAlpha
title: ITextFont2::SetAutospaceAlpha
author: windows-sdk-content
description: Sets the East Asian &#0034;autospace alpha&#0034; state.
old-location: controls\itextfont2_setautospacealpha.htm
tech.root: controls
ms.assetid: 8a01677d-74c6-437b-8ee9-350c891c6c3f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetAutospaceAlpha method, ITextFont2.SetAutospaceAlpha, ITextFont2::SetAutospaceAlpha, SetAutospaceAlpha, SetAutospaceAlpha method [Windows Controls], SetAutospaceAlpha method [Windows Controls],ITextFont2 interface, controls.itextfont2_setautospacealpha, tom/ITextFont2::SetAutospaceAlpha
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
 - ITextFont2.SetAutospaceAlpha
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont2::SetAutospaceAlpha


## -description


Sets the East Asian "autospace alpha" state.


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
<td>Use East Asian autospace alphabetics.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not use East Asian autospace alphabetics.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the AutospaceAlpha property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The AutospaceAlpha property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/3f2070e9-2909-4642-ade2-54ef9af9cfc8">ITextFont2::GetAutospaceAlpha</a>
 

 

