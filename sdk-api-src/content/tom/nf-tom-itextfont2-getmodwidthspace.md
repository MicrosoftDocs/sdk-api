---
UID: NF:tom.ITextFont2.GetModWidthSpace
title: ITextFont2::GetModWidthSpace (tom.h)
author: windows-sdk-content
description: Gets whether &#0034;increase width of whitespace&#0034; is active.
old-location: controls\itextfont2_getmodwidthspace.htm
tech.root: Controls
ms.assetid: 6ce6250f-94e6-4a20-89cd-f3e9a83a9408
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetModWidthSpace, GetModWidthSpace method [Windows Controls], GetModWidthSpace method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetModWidthSpace method, ITextFont2.GetModWidthSpace, ITextFont2::GetModWidthSpace, controls.itextfont2_getmodwidthspace, tom/ITextFont2::GetModWidthSpace
ms.topic: method
f1_keywords: 
 - "tom/ITextFont2.GetModWidthSpace"
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
 - ITextFont2.GetModWidthSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextFont2::GetModWidthSpace


## -description


Gets whether "increase width of whitespace" is active.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="https://docs.microsoft.com/windows/desktop/Controls/about-text-object-model">tomBool</a> value that can be one of the following.

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



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setmodwidthspace">ITextFont2::SetModWidthSpace</a>
 

 

