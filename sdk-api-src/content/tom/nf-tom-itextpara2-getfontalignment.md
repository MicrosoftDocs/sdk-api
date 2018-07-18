---
UID: NF:tom.ITextPara2.GetFontAlignment
title: ITextPara2::GetFontAlignment
author: windows-sdk-content
description: Gets the paragraph font alignment state.
old-location: controls\itextpara2_getfontalignment.htm
old-project: controls
ms.assetid: 1064c033-2ae0-46ec-a670-603edd673e87
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetFontAlignment, GetFontAlignment method [Windows Controls], GetFontAlignment method [Windows Controls],ITextPara2 interface, ITextPara2 interface [Windows Controls],GetFontAlignment method, ITextPara2.GetFontAlignment, ITextPara2::GetFontAlignment, controls.itextpara2_getfontalignment, tom/ITextPara2::GetFontAlignment
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
 - ITextPara2.GetFontAlignment
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara2::GetFontAlignment


## -description


Gets the paragraph font alignment state.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The paragraph font alignment state. It can be one of the following values.

<table>
<tr>
<th>Font Alignment States</th>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/library/Hh768766(v=VS.85).aspx">tomFontAlignmentAuto</a> (default)</td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/library/Hh768766(v=VS.85).aspx">tomFontAlignmentTop</a></td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/library/Hh768766(v=VS.85).aspx">tomFontAlignmentBaseline</a></td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/library/Hh768766(v=VS.85).aspx">tomFontAlignmentBottom</a></td>
</tr>
<tr>
<td><a href="https://msdn.microsoft.com/library/Hh768766(v=VS.85).aspx">tomFontAlignmentCenter</a></td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>



<a href="https://msdn.microsoft.com/2ed1f7f2-9523-4dda-bac0-c1eb3d217102">ITextPara2::SetFontAlignment</a>
 

 

