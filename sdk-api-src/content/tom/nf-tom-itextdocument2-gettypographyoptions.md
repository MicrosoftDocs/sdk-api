---
UID: NF:tom.ITextDocument2.GetTypographyOptions
title: ITextDocument2::GetTypographyOptions (tom.h)
author: windows-sdk-content
description: Gets the typography options.
old-location: controls\itextdocument2_gettypographyoptions.htm
tech.root: Controls
ms.assetid: 3433954c-818b-4811-9e38-4bc8ab3ee7f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTypographyOptions, GetTypographyOptions method [Windows Controls], GetTypographyOptions method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetTypographyOptions method, ITextDocument2.GetTypographyOptions, ITextDocument2::GetTypographyOptions, TO_ADVANCEDTYPOGRAPHY, TO_SIMPLELINEBREAK, controls.itextdocument2_gettypographyoptions, tom/ITextDocument2::GetTypographyOptions
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
 - ITextDocument2.GetTypographyOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextDocument2::GetTypographyOptions


## -description


Gets the typography options.


## -parameters




### -param pOptions [out, retval]

Type: <b>long*</b>

A combination of the following typography options. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TO_ADVANCEDTYPOGRAPHY"></a><a id="to_advancedtypography"></a><dl>
<dt><b>TO_ADVANCEDTYPOGRAPHY</b></dt>
</dl>
</td>
<td width="60%">
Advanced typography (special line breaking and line formatting) is turned on.

</td>
</tr>
<tr>
<td width="40%"><a id="TO_SIMPLELINEBREAK"></a><a id="to_simplelinebreak"></a><dl>
<dt><b>TO_SIMPLELINEBREAK</b></dt>
</dl>
</td>
<td width="60%">
Normal line breaking and formatting is used.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/1013c9bf-b6fe-4396-b7a8-36e61edf1df3">ITextDocument2::SetTypographyOptions</a>
 

 

