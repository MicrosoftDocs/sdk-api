---
UID: NF:tom.ITextFont2.GetDoubleStrike
title: ITextFont2::GetDoubleStrike
author: windows-sdk-content
description: Gets whether characters are displayed with double horizontal lines through the center.
old-location: controls\itextfont2_getdoublestrike.htm
old-project: Controls
ms.assetid: 9e599c29-4b47-4043-b9c7-75a736ca64fa
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetDoubleStrike, GetDoubleStrike method [Windows Controls], GetDoubleStrike method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetDoubleStrike method, ITextFont2.GetDoubleStrike, ITextFont2::GetDoubleStrike, controls.itextfont2_getdoublestrike, tom/ITextFont2::GetDoubleStrike
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
-	ITextFont2.GetDoubleStrike
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetDoubleStrike


## -description


Gets whether characters are displayed with double horizontal lines through the center.


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
<td>Characters are displayed with double horizontal lines.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not displayed with double horizontal lines.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The DoubleStrike property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/bed8ce93-5c3a-43ee-b9c7-c1fd42481bbd">ITextFont2::SetDoubleStrike</a>
 

 

