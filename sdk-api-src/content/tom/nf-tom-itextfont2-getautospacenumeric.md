---
UID: NF:tom.ITextFont2.GetAutospaceNumeric
title: ITextFont2::GetAutospaceNumeric
author: windows-sdk-content
description: Gets the East Asian &#0034;autospace numeric&#0034; state.
old-location: controls\itextfont2_getautospacenumeric.htm
old-project: Controls
ms.assetid: 448a461b-779a-457e-8206-2055a73c9b45
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetAutospaceNumeric, GetAutospaceNumeric method [Windows Controls], GetAutospaceNumeric method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetAutospaceNumeric method, ITextFont2.GetAutospaceNumeric, ITextFont2::GetAutospaceNumeric, controls.itextfont2_getautospacenumeric, tom/ITextFont2::GetAutospaceNumeric
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextFont2.GetAutospaceNumeric
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetAutospaceNumeric


## -description


Gets the East Asian "autospace numeric" state.


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
<td>Use East Asian autospace numerics.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not use East Asian autospace numerics.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The AutospaceNumeric property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/7fd911c2-a765-4bbc-a14c-15665d5a4a16">ITextFont2::SetAutospaceNumeric</a>
 

 

