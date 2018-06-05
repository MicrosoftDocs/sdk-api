---
UID: NF:tom.ITextFont2.GetModWidthSpace
title: ITextFont2::GetModWidthSpace
author: windows-sdk-content
description: Gets whether &#0034;increase width of whitespace&#0034; is active.
old-location: controls\itextfont2_getmodwidthspace.htm
old-project: Controls
ms.assetid: 6ce6250f-94e6-4a20-89cd-f3e9a83a9408
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetModWidthSpace, GetModWidthSpace method [Windows Controls], GetModWidthSpace method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetModWidthSpace method, ITextFont2.GetModWidthSpace, ITextFont2::GetModWidthSpace, controls.itextfont2_getmodwidthspace, tom/ITextFont2::GetModWidthSpace
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextFont2.GetModWidthSpace
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetModWidthSpace


## -description


Gets whether "increase width of whitespace" is active.


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
<td>Increase width of whitespace is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Increase width of whitespace is not active.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The ModWidthSpace property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/df3ea127-1f47-4173-ad2c-0a7af4c8454c">ITextFont2::SetModWidthSpace</a>
 

 

