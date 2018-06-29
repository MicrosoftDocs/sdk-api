---
UID: NF:tom.ITextFont2.GetOldNumbers
title: ITextFont2::GetOldNumbers
author: windows-sdk-content
description: Gets whether old-style numbers are active.
old-location: controls\itextfont2_getoldnumbers.htm
old-project: Controls
ms.assetid: 8e800840-5ca2-4fbf-94c2-d51aa73bf188
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetOldNumbers, GetOldNumbers method [Windows Controls], GetOldNumbers method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetOldNumbers method, ITextFont2.GetOldNumbers, ITextFont2::GetOldNumbers, controls.itextfont2_getoldnumbers, tom/ITextFont2::GetOldNumbers
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
 - ITextFont2.GetOldNumbers
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetOldNumbers


## -description


Gets whether old-style numbers are active.


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
<td>Old-style numbers are active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Old-style numbers are not active.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The OldNumbers property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/f510781e-ede9-41dc-ae69-3b0ca52a6773">ITextFont2::SetOldNumbers</a>
 

 

