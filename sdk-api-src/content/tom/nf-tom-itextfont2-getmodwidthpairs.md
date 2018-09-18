---
UID: NF:tom.ITextFont2.GetModWidthPairs
title: ITextFont2::GetModWidthPairs
author: windows-sdk-content
description: Gets whether &#0034;decrease widths on pairs&#0034; is active.
old-location: controls\itextfont2_getmodwidthpairs.htm
tech.root: Controls
ms.assetid: 8fcbc781-42da-46aa-b231-3a8246eccd36
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetModWidthPairs, GetModWidthPairs method [Windows Controls], GetModWidthPairs method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetModWidthPairs method, ITextFont2.GetModWidthPairs, ITextFont2::GetModWidthPairs, controls.itextfont2_getmodwidthpairs, tom/ITextFont2::GetModWidthPairs
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
 - ITextFont2.GetModWidthPairs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont2::GetModWidthPairs


## -description


Gets whether "decrease widths on pairs" is active.


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
<td>Decrease widths on pairs is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Decrease widths on pairs is not active.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The ModWidthPairs property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/60117c84-18f9-49db-8d13-b55576874d2b">ITextFont2::SetModWidthPairs</a>
 

 

